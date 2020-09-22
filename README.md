<div align="center">

## \_String Replace \(for real\)


</div>

### Description

Replaces all occurances of a given substring with another substring in a String object.

I looked for a good string replacer and all of them broke (replaced things multiple times, infinitely looped, etc), so I made one. Please let me know if this doesn't work, because if it doesn't work for you then it doesn't work for me! Thanks.
 
### More Info
 
aSearch=The String to search

aFind=The String to find

aReplace=The String to replace aFind with

Returns aSearch with all occurances of aFind replaced with aReplace


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Atul Brad Buono](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/atul-brad-buono.md)
**Level**          |Beginner
**User Rating**    |4.5 (27 globes from 6 users)
**Compatibility**  |Java \(JDK 1\.2\)
**Category**       |[String Manipulation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/string-manipulation__2-60.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/atul-brad-buono-string-replace-for-real__2-2433/archive/master.zip)





### Source Code

```
public static String replaceString(String aSearch, String aFind, String aReplace)
{
 String result = aSearch;
 if (result != null && result.length() > 0)
 {
  int a = 0;
  int b = 0;
  while (true)
  {
   a = result.indexOf(aFind, b);
   if (a != -1)
   {
    result = result.substring(0, a) + aReplace + result.substring(a + aFind.length());
    b = a + aReplace.length();
   }
   else
    break;
  }
 }
 return result;
}
```

