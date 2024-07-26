package com.mycompany.mavenproject3;

import java.util.Scanner;

/**
 *
 * @author PC
 */
public class Mavenproject3 {

    public static void main(String[] args) 
    {
        Scanner num = new Scanner(System.in);
        String Name;
        
        System.out.println("Name:");
        Name = num.nextLine();
        int logname = Name.length();
        
        int a = 0;
        int b = 0;
        int c = -1; 
        
        for (int i = 0; i < logname; i++) 
        {
            if (Name.charAt(i) == ' ')
            {
                c = i;
                break; 
            }                  
        }
        
        String Aname;
        String Bname;
        
        if (c == -1) 
        {
            Aname = Name;
            Bname = "";
        }
        else 
        {
            Aname = Name.substring(0, c);
            Bname = Name.substring(c+1 , logname);
        }
        
        System.out.println("FirstName: " + Aname);
        System.out.println("LastName: " + Bname);
    }
}
