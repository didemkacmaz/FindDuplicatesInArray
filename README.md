# FindDuplicatesInArray
```
package com.didem;

import java.util.HashMap;
import java.util.Map;

public class FindDuplicatesInArray {

	public static void main(String[] args) {
		String[] strArray = {"Java", "JSP", "Servlets", "Java", "Struts", "JSP", "JDBC", "JSP", "JSP", "JSP", "JSP", "JSP"};
		HashMap<String, Integer> counter = new HashMap<String, Integer>();
				
		for(String str : strArray){
			if(counter.containsKey(str)){
				counter.put(str, counter.get(str)+1);
			}else{
				counter.put(str, 1);
			}
		}
		
		for (Map.Entry<String, Integer> entry : counter.entrySet()) {
			System.out.println("The Repeated value is : " + entry.getKey() + " Count is : " + entry.getValue());
		}

	}
}
```
