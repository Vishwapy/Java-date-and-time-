# Java-date-and-time

import java.io.*;
import java.math.*;
import java.security.*;
import java.util.Calendar;
import java.util.List;
import java.util.Arrays;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;

public class JavaDateAndTime {
    static List<String> days = Arrays.asList("SUNDAY", "MONDAY", "TUESDAY", "WEDNESDAY", "THURSDAY", "FRIDAY", "SATURDAY");
    
    public static String getDay(String day, String month, String year) {
          
        int y = Integer.parseInt(year);
        int m = Integer.parseInt(month);
        int d = Integer.parseInt(day);
          
        Calendar c = Calendar.getInstance();
        c.set(y, m-1, d); 
            
        int p = c.get(Calendar.DAY_OF_WEEK);
        String s = days.get(p-1);
        return s;
    }
    
    public static void main(String[] args) {
        Scanner in = new Scanner(System.in);
        String month = in.next();
        String day = in.next();
        String year = in.next();
        
        System.out.println(getDay(day, month, year));
        
    }
}

