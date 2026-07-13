---
UID: NF:winbase.GetPrivateProfileStringA
title: GetPrivateProfileStringA function (winbase.h)
description: Retrieves a string from the specified section in an initialization file. (GetPrivateProfileStringA)
helpviewer_keywords: ["GetPrivateProfileStringA", "winbase/GetPrivateProfileStringA"]
old-location: base\getprivateprofilestring.htm
tech.root: winprog
ms.assetid: 684bae93-3cd8-49a4-8f16-9316df41d6f2
ms.date: 12/05/2018
ms.keywords: GetPrivateProfileString, GetPrivateProfileString function, GetPrivateProfileStringA, GetPrivateProfileStringW, _win32_getprivateprofilestring, base.getprivateprofilestring, winbase/GetPrivateProfileString, winbase/GetPrivateProfileStringA, winbase/GetPrivateProfileStringW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetPrivateProfileStringW (Unicode) and GetPrivateProfileStringA (ANSI)
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
ms.custom: snippet-project
f1_keywords:
 - GetPrivateProfileStringA
 - winbase/GetPrivateProfileStringA
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
 - GetPrivateProfileString
 - GetPrivateProfileStringA
 - GetPrivateProfileStringW
---

# GetPrivateProfileStringA function


## -description

Retrieves a string from the specified section in an initialization file.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit Windows-based applications. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpAppName [in]

The name of the section containing the key name. If this parameter is <b>NULL</b>, the 
<b>GetPrivateProfileString</b> function copies all section names in the file to the supplied buffer.

### -param lpKeyName [in]

The name of the key whose associated string is to be retrieved. If this parameter is <b>NULL</b>, all key names in the section specified by the <i>lpAppName</i> parameter are copied to the buffer specified by the <i>lpReturnedString</i> parameter.

### -param lpDefault [in]

A default string. If the <i>lpKeyName</i> key cannot be found in the initialization file, 
<b>GetPrivateProfileString</b> copies the default string to the <i>lpReturnedString</i> buffer.  


If this parameter is <b>NULL</b>, the default is an empty string, "".

Avoid specifying a default string with trailing blank characters. The function inserts a <b>null</b> character in the <i>lpReturnedString</i> buffer to strip any trailing blanks.

### -param lpReturnedString [out]

A pointer to the buffer that receives the retrieved string.

### -param nSize [in]

The size of the buffer pointed to by the <i>lpReturnedString</i> parameter, in characters.

### -param lpFileName [in]

The name of the initialization file. If this parameter does not contain a full path to the file, the system searches for the file in the Windows directory.

## -returns

The return value is the number of characters copied to the buffer, not including the terminating <b>null</b> character.

If neither <i>lpAppName</i> nor <i>lpKeyName</i> is <b>NULL</b> and the supplied destination buffer is too small to hold the requested string, the string is truncated and followed by a <b>null</b> character, and the return value is equal to <i>nSize</i> minus one.

If either <i>lpAppName</i> or <i>lpKeyName</i> is <b>NULL</b> and the supplied destination buffer is too small to hold all the strings, the last string is truncated and followed by two <b>null</b> characters. In this case, the return value is equal to <i>nSize</i> minus two.

In the event the initialization file specified by <i>lpFileName</i> is not found, or contains invalid values, this function will set <b>errorno</b> with a value of '0x2' (File Not Found). To retrieve extended error information, call <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The 
<b>GetPrivateProfileString</b> function searches the specified initialization file for a key that matches the name specified by the <i>lpKeyName</i> parameter under the section heading specified by the <i>lpAppName</i> parameter. If it finds the key, the function copies the corresponding string to the buffer. If the key does not exist, the function copies the default character string specified by the <i>lpDefault</i> parameter. A section in the initialization file must have the following form:
				
			


``` syntax
[section]
key=string
      .
      .
      .
```

If <i>lpAppName</i> is <b>NULL</b>, 
<b>GetPrivateProfileString</b> copies all section names in the specified file to the supplied buffer. If <i>lpKeyName</i> is <b>NULL</b>, the function copies all key names in the specified section to the supplied buffer. An application can use this method to enumerate all of the sections and keys in a file. In either case, each string is followed by a <b>null</b> character and the final string is followed by a second <b>null</b> character. If the supplied destination buffer is too small to hold all the strings, the last string is truncated and followed by two <b>null</b> characters.

If the string associated with <i>lpKeyName</i> is enclosed in single or double quotation marks, the marks are discarded when the 
<b>GetPrivateProfileString</b> function retrieves the string.

The 
<b>GetPrivateProfileString</b> function is not case-sensitive; the strings can be a combination of uppercase and lowercase letters.

To retrieve a string from the Win.ini file, use the 
<a href="/windows/desktop/api/winbase/nf-winbase-getprofilestringa">GetProfileString</a> function.

The system maps most .ini file references to the registry, using the mapping defined under the following registry key:<b>HKEY_LOCAL_MACHINE</b>&#92;<b>SOFTWARE</b>&#92;<b>Microsoft</b>&#92;<b>Windows NT</b>&#92;<b>CurrentVersion</b>&#92;<b>IniFileMapping</b>



This mapping is likely if an application modifies system-component initialization files, such as Control.ini, System.ini, and Winfile.ini. In these cases, the 
function retrieves information from the registry, not from the initialization file; the change in the storage location has no effect on the function's behavior.

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


## Example

The following example demonstrates the use of **GetPrivateProfileString**.

```cpp
// Gets a profile string called "Preferred line" and converts it to an int.
GetPrivateProfileString (
      "Preference",
      "Preferred Line",
      gszNULL, 
      szBuffer,
      MAXBUFSIZE,
      gszINIfilename
);

// if szBuffer is not empty.
if ( lstrcmp ( gszNULL, szBuffer ) )
{
      dwPreferredPLID = (DWORD) atoi( szBuffer );	
}
else	
{
      dwPreferredPLID = (DWORD) -1;
}
```

> [!NOTE]
> The winbase.h header defines GetPrivateProfileString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprofilestringa">GetProfileString</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeprivateprofilestringa">WritePrivateProfileString</a>
