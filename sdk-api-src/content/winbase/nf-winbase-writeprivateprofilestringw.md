---
UID: NF:winbase.WritePrivateProfileStringW
title: WritePrivateProfileStringW function (winbase.h)
description: Copies a string into the specified section of an initialization file. (Unicode)
helpviewer_keywords: ["WritePrivateProfileString", "WritePrivateProfileString function", "WritePrivateProfileStringW", "_win32_writeprivateprofilestring", "base.writeprivateprofilestring", "winbase/WritePrivateProfileString", "winbase/WritePrivateProfileStringW"]
old-location: base\writeprivateprofilestring.htm
tech.root: winprog
ms.assetid: f0799092-c6c1-4800-a17a-fcf744b1228f
ms.date: 12/05/2018
ms.keywords: WritePrivateProfileString, WritePrivateProfileString function, WritePrivateProfileStringA, WritePrivateProfileStringW, _win32_writeprivateprofilestring, base.writeprivateprofilestring, winbase/WritePrivateProfileString, winbase/WritePrivateProfileStringA, winbase/WritePrivateProfileStringW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WritePrivateProfileStringW (Unicode) and WritePrivateProfileStringA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WritePrivateProfileStringW
 - winbase/WritePrivateProfileStringW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Privateprofile-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Privateprofile-l1-1-1.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
api_name:
 - WritePrivateProfileString
 - WritePrivateProfileStringA
 - WritePrivateProfileStringW
---

# WritePrivateProfileStringW function


## -description

Copies a string into the specified section of an initialization file.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpAppName [in]

The name of the section to which the string will be copied. If the section does not exist, it is created. The name of the section is case-independent; the string can be any combination of uppercase and lowercase letters.

### -param lpKeyName [in]

The name of the key to be associated with a string. If the key does not exist in the specified section, it is created. If this parameter is <b>NULL</b>, the entire section, including all entries within the section, is deleted.

### -param lpString [in]

A <b>null</b>-terminated string to be written to the file. If this parameter is <b>NULL</b>, the key pointed to by the <i>lpKeyName</i> parameter is deleted.

### -param lpFileName [in]

The name of the initialization file.

If the file already exists and consists of Unicode characters, the function writes Unicode characters to the file. Otherwise, the function writes ANSI characters.

## -returns

If the function successfully copies the string to the initialization file, the return value is nonzero.

If the function fails, or if it flushes the cached version of the most recently accessed initialization file, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A section in the initialization file must have the following form:


``` syntax
[section]
key=string
      .
      .
      .
```

If the <i>lpFileName</i> parameter does not contain a full path and file name for the file, 
<b>WritePrivateProfileString</b> searches the Windows directory for the file. If the file does not exist, this function creates the file in the Windows directory.

If <i>lpFileName</i> contains a full path and file name and the file does not exist, 
<b>WritePrivateProfileString</b> creates the file. The specified directory must already exist.

The system keeps a cached version of the most recent registry file mapping to improve performance. If all parameters are <b>NULL</b>, the function flushes the cache. While the system is editing the cached version of the file, processes that edit the file itself will use the original file until the cache has been cleared.

The system maps most .ini file references to the registry, using the mapping defined under the following registry key:<pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>IniFileMapping</b></pre>


This mapping is likely if an application modifies system-component initialization files, such as Control.ini, System.ini, and Winfile.ini. In this case, the 
function writes information to the registry, not to the initialization file; the change in the storage location has no effect on the function's behavior.

The profile functions use the following steps to locate initialization information:
				

<ol>
<li>Look in the registry for the name of the initialization file  under the <b>IniFileMapping</b> key.</li>
<li>Look for the section name specified by <i>lpAppName</i>. This will be a named value under the key that has the name of the initialization file, or a subkey with this name, or the name will not exist as either a value or subkey.</li>
<li>If the section name specified by <i>lpAppName</i> is a named value, then that value specifies where in the registry you will find the keys for the section.</li>
<li>If the section name specified by <i>lpAppName</i> is a subkey, then named values under that subkey specify where in the registry you will find the keys for the section. If the key you are looking for does not exist as a named value, then there will be an unnamed value (shown as <b>&lt;No Name&gt;</b>) that specifies the default location in the registry where you will find the key.</li>
<li>If the section name specified by <i>lpAppName</i> does not exist as a named value or as a subkey, then there will be an unnamed value (shown as <b>&lt;No Name&gt;</b>) that specifies the default location in the registry where you will find the keys for the section.</li>
<li>If there is no subkey or entry for the section name, then look for the actual initialization file on the disk and read its contents.</li>
</ol>
When looking at values in the registry that specify other registry locations, there are several prefixes that change the behavior of the .ini file mapping:
				
			

<ul>
<li>! - this character forces all writes to go both to the registry and to the .ini file on disk.</li>
<li># - this character causes the registry value to be set to the value in the Windows 3.1 .ini file when a new user logs in for the first time after setup.</li>
<li>@ - this character prevents any reads from going to the .ini file on disk if the requested data is not found in the registry.</li>
<li>USR: - this prefix stands for <b>HKEY_CURRENT_USER</b>, and the text after the prefix is relative to that key.</li>
<li>SYS: - this prefix stands for <b>HKEY_LOCAL_MACHINE\SOFTWARE</b>, and the text after the prefix is relative to that key.</li>
</ul>
An application using the <b>WritePrivateProfileString</b> function to enter .ini file information into the registry should follow these guidelines:

<ul>
<li>Ensure that no .ini file of the specified name exists on the system.</li>
<li>Ensure that there is a key entry in the registry that specifies the .ini file. This entry should be under the path <b>HKEY_LOCAL_MACHINE\SOFTWARE \Microsoft\Windows NT\CurrentVersion\IniFileMapping</b>.</li>
<li>Specify a value for that .ini file key entry that specifies a section. That is to say, an application must specify a section name, as it would appear within an .ini file or registry entry. Here is an example: [My Section].</li>
<li>For system files, specify SYS for an added value.</li>
<li>For application files, specify USR within the added value. Here is an example: "My Section: USR: App Name\Section". And, since USR indicates a mapping under <b>HKEY_CURRENT_USER</b>, the application should also create a key under <b>HKEY_CURRENT_USER</b> that specifies the application name listed in the added value. For the example just given, that would be "App Name".</li>
<li>After following the preceding steps, an application setup program should call <b>WritePrivateProfileString</b> with the first three parameters set to <b>NULL</b>, and the fourth parameter set to the INI file name. For example: 


<code>WritePrivateProfileString( NULL, NULL, NULL, L"appname.ini" );</code>

</li>
<li>Such a call causes the mapping of an .ini file to the registry to take effect before the next system reboot. The system rereads the mapping information into shared memory. A user will not have to reboot their computer after installing an application in order to have future invocations of the application see the mapping of the .ini file to the registry.</li>
</ul>

#### Examples

The following sample code illustrates the preceding guidelines and is based on several assumptions:

<ul>
<li>There is an application named App Name.</li>
<li>That application uses an .ini file named AppName.ini.</li>
<li>There is a section in the .ini file that we want to look like this: 



``` syntax
[Section1] 
  FirstKey = It all worked out okay. 
  SecondKey = By golly, it works. 
  ThirdKey = Another test.
```

</li>
<li>The user will not have to reboot the system in order to have future invocations of the application see the mapping of the .ini file to the registry.</li>
</ul>

```cpp
#include <windows.h> 
#include <tchar.h>
#include <stdio.h> 
 
int main() 
{ 
   TCHAR   inBuf[80]; 
   HKEY   hKey1, hKey2; 
   DWORD  dwDisposition; 
   LONG   lRetCode; 
   TCHAR   szData[] = TEXT("USR:App Name\\Section1");
 
   // Create the .ini file key. 
   lRetCode = RegCreateKeyEx ( HKEY_LOCAL_MACHINE, 
       TEXT("SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion\\IniFileMapping\\appname.ini"), 
       0, 
       NULL, 
       REG_OPTION_NON_VOLATILE, 
       KEY_WRITE, 
       NULL, 
       &hKey1, 
       &dwDisposition); 
 
   if (lRetCode != ERROR_SUCCESS)
   { 
      printf ("Error in creating appname.ini key (%d).\n", lRetCode); 
      return (0) ; 
   } 
 
   // Set a section value 
   lRetCode = RegSetValueEx ( hKey1, 
                              TEXT("Section1"), 
                              0, 
                              REG_SZ, 
                              (BYTE *)szData, 
                              sizeof(szData)); 
 
   if (lRetCode != ERROR_SUCCESS) 
   { 
      printf ("Error in setting Section1 value\n"); 
      // Close the key
      lRetCode = RegCloseKey( hKey1 );
      if( lRetCode != ERROR_SUCCESS )
      {
         printf("Error in RegCloseKey (%d).\n", lRetCode);
         return (0) ; 
      }
   } 
 
   // Create an App Name key 
   lRetCode = RegCreateKeyEx ( HKEY_CURRENT_USER, 
                               TEXT("App Name"), 
                               0, 
                               NULL, 
                               REG_OPTION_NON_VOLATILE,
                               KEY_WRITE, 
                               NULL, 
                               &hKey2, 
                               &dwDisposition); 
 
   if (lRetCode != ERROR_SUCCESS) 
   { 
      printf ("Error in creating App Name key (%d).\n", lRetCode); 

      // Close the key
      lRetCode = RegCloseKey( hKey2 );
      if( lRetCode != ERROR_SUCCESS )
      {
         printf("Error in RegCloseKey (%d).\n", lRetCode);
         return (0) ; 
      }
   } 
 
   // Force the system to read the mapping into shared memory 
   // so that future invocations of the application will see it 
   // without the user having to reboot the system 
   WritePrivateProfileStringW( NULL, NULL, NULL, L"appname.ini" ); 
 
   // Write some added values 
   WritePrivateProfileString (TEXT("Section1"), 
                              TEXT("FirstKey"), 
                              TEXT("It all worked out OK."), 
                              TEXT("appname.ini")); 
   WritePrivateProfileString (TEXT("Section1"), 
                              TEXT("SecondKey"), 
                              TEXT("By golly, it works!"), 
                              TEXT("appname.ini")); 
   WritePrivateProfileString (TEXT("Section1"), 
                              TEXT("ThirdKey"), 
                              TEXT("Another test..."), 
                              TEXT("appname.ini")); 

   // Test 
   GetPrivateProfileString (TEXT("Section1"), 
                            TEXT("FirstKey"), 
                            TEXT("Error: GPPS failed"), 
                            inBuf, 
                            80, 
                            TEXT("appname.ini")); 
   _tprintf (TEXT("Key: %s\n"), inBuf); 
 
   // Close the keys
   lRetCode = RegCloseKey( hKey1 );
   if( lRetCode != ERROR_SUCCESS )
   {
      printf("Error in RegCloseKey (%d).\n", lRetCode);
      return(0);
   }

   lRetCode = RegCloseKey( hKey2 );
   if( lRetCode != ERROR_SUCCESS )
   {
      printf("Error in RegCloseKey (%d).\n", lRetCode);
      return(0);
   }
   
   return(1); 
}

```






> [!NOTE]
> The winbase.h header defines WritePrivateProfileString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring">GetPrivateProfileString</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeprofilestringa">WriteProfileString</a>
