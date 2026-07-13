---
UID: NF:winbase.GetProfileStringW
title: GetProfileStringW function (winbase.h)
description: Retrieves the string associated with a key in the specified section of the Win.ini file. (Unicode)
helpviewer_keywords: ["GetProfileString", "GetProfileString function", "GetProfileStringW", "_win32_getprofilestring", "base.getprofilestring", "winbase/GetProfileString", "winbase/GetProfileStringW"]
old-location: base\getprofilestring.htm
tech.root: winprog
ms.assetid: 70987969-7ad5-4eb6-bcd0-ce8709864ee7
ms.date: 12/05/2018
ms.keywords: GetProfileString, GetProfileString function, GetProfileStringA, GetProfileStringW, _win32_getprofilestring, base.getprofilestring, winbase/GetProfileString, winbase/GetProfileStringA, winbase/GetProfileStringW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetProfileStringW (Unicode) and GetProfileStringA (ANSI)
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
 - GetProfileStringW
 - winbase/GetProfileStringW
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
 - GetProfileString
 - GetProfileStringA
 - GetProfileStringW
---

# GetProfileStringW function


## -description

Retrieves the string associated with a key in the specified section of the Win.ini file.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit Windows-based applications, therefore this function should not be called from server code. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpAppName [in]

The name of the section containing the key. If this parameter is <b>NULL</b>, the function copies all section names in the file to the supplied buffer.

### -param lpKeyName [in]

The name of the key whose associated string is to be retrieved. If this parameter is <b>NULL</b>, the function copies all keys in the given section to the supplied buffer. Each string is followed by a <b>null</b> character, and the final string is followed by a second <b>null</b> character.

### -param lpDefault [in]

A default string. If the <i>lpKeyName</i> key cannot be found in the initialization file, 
<b>GetProfileString</b> copies the default string to the <i>lpReturnedString</i> buffer. If this parameter is <b>NULL</b>, the default is an empty string, "". 




Avoid specifying a default string with trailing blank characters. The function inserts a <b>null</b> character in the <i>lpReturnedString</i> buffer to strip any trailing blanks.

### -param lpReturnedString [out]

A pointer to a buffer that receives the character string.

### -param nSize [in]

The size of the buffer pointed to by the <i>lpReturnedString</i> parameter, in characters.

## -returns

The return value is the number of characters copied to the buffer, not including the <b>null</b>-terminating character.

If neither <i>lpAppName</i> nor <i>lpKeyName</i> is <b>NULL</b> and the supplied destination buffer is too small to hold the requested string, the string is truncated and followed by a <b>null</b> character, and the return value is equal to <i>nSize</i> minus one.

If either <i>lpAppName</i> or <i>lpKeyName</i> is <b>NULL</b> and the supplied destination buffer is too small to hold all the strings, the last string is truncated and followed by two <b>null</b> characters. In this case, the return value is equal to <i>nSize</i> minus two.

## -remarks

If the string associated with the <i>lpKeyName</i> parameter is enclosed in single or double quotation marks, the marks are discarded when the 
<b>GetProfileString</b> function returns the string.

The 
<b>GetProfileString</b> function is not case-sensitive; the strings can contain a combination of uppercase and lowercase letters.

A section in the Win.ini file must have the following form: 


``` syntax
[section]
key=string
      .
      .
      .
```

An application can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring">GetPrivateProfileString</a> function to retrieve a string from a specified initialization file.

The <i>lpDefault</i> parameter must point to a valid string, even if the string is empty (that is, even if its first character is a <b>null</b> character).

<b>Windows Server 2003 and Windows XP/2000:  </b>Calls to profile functions may be mapped to the registry instead of to the initialization files. This mapping occurs when the initialization file and section are specified in the registry under the following keys:<p class="note">
<b>HKEY_LOCAL_MACHINE</b>&#92;<b>Software</b>&#92;<b>Microsoft</b>&#92;<b>Windows NT</b>&#92;<b>CurrentVersion</b>&#92;<b>IniFileMapping</b>





When the operation has been mapped, the 
<b>GetProfileString</b> function retrieves information from the registry, not from the initialization file; the change in the storage location has no effect on the function's behavior.

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




> [!NOTE]
> The winbase.h header defines GetProfileString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring">GetPrivateProfileString</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeprofilestringa">WriteProfileString</a>
