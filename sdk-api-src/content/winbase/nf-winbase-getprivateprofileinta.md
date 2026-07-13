---
UID: NF:winbase.GetPrivateProfileIntA
title: GetPrivateProfileIntA function (winbase.h)
description: Retrieves an integer associated with a key in the specified section of an initialization file. (GetPrivateProfileIntA)
helpviewer_keywords: ["GetPrivateProfileIntA", "winbase/GetPrivateProfileIntA"]
old-location: base\getprivateprofileint.htm
tech.root: winprog
ms.assetid: dcb48ec3-7172-4bcc-a833-23e34a73d70b
ms.date: 12/05/2018
ms.keywords: GetPrivateProfileInt, GetPrivateProfileInt function, GetPrivateProfileIntA, GetPrivateProfileIntW, _win32_getprivateprofileint, base.getprivateprofileint, winbase/GetPrivateProfileInt, winbase/GetPrivateProfileIntA, winbase/GetPrivateProfileIntW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetPrivateProfileIntW (Unicode) and GetPrivateProfileIntA (ANSI)
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
 - GetPrivateProfileIntA
 - winbase/GetPrivateProfileIntA
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
 - GetPrivateProfileInt
 - GetPrivateProfileIntA
 - GetPrivateProfileIntW
---

# GetPrivateProfileIntA function


## -description

Retrieves an integer associated with a key in the specified section of an initialization file.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit Windows-based applications. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpAppName [in]

The name of the section in the initialization file.

### -param lpKeyName [in]

The name of the key whose value is to be retrieved. This value is in the form of a string; the 
<b>GetPrivateProfileInt</b> function converts the string into an integer and returns the integer.

### -param nDefault [in]

The default value to return if the key name cannot be found in the initialization file.

### -param lpFileName [in]

The name of the initialization file. If this parameter does not contain a full path to the file, the system searches for the file in the Windows directory.

## -returns

The return value is the integer equivalent of the string following the specified key name in the specified initialization file. If the key is not found, the return value is the specified default value.

## -remarks

The function searches the file for a key that matches the name specified by the <i>lpKeyName</i> parameter under the section name specified by the <i>lpAppName</i> parameter. A section in the initialization file must have the following form:


``` syntax
[section]
key=value
      .
      .
      .
```

The 
<b>GetPrivateProfileInt</b> function is not case-sensitive; the strings in <i>lpAppName</i> and <i>lpKeyName</i> can be a combination of uppercase and lowercase letters.

An application can use the 
<a href="/windows/desktop/api/winbase/nf-winbase-getprofileinta">GetProfileInt</a> function to retrieve an integer value from the Win.ini file.

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




> [!NOTE]
> The winbase.h header defines GetPrivateProfileInt as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprofileinta">GetProfileInt</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeprivateprofilestringa">WritePrivateProfileString</a>
