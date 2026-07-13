---
UID: NF:winbase.WritePrivateProfileStructA
title: WritePrivateProfileStructA function (winbase.h)
description: Copies data into a key in the specified section of an initialization file. As it copies the data, the function calculates a checksum and appends it to the end of the data. (ANSI)
helpviewer_keywords: ["WritePrivateProfileStructA", "winbase/WritePrivateProfileStructA"]
old-location: base\writeprivateprofilestruct.htm
tech.root: winprog
ms.assetid: 21b1927c-40b0-4b79-931b-6d3db176fb71
ms.date: 12/05/2018
ms.keywords: WritePrivateProfileStruct, WritePrivateProfileStruct function, WritePrivateProfileStructA, WritePrivateProfileStructW, _win32_writeprivateprofilestruct, base.writeprivateprofilestruct, winbase/WritePrivateProfileStruct, winbase/WritePrivateProfileStructA, winbase/WritePrivateProfileStructW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WritePrivateProfileStructW (Unicode) and WritePrivateProfileStructA (ANSI)
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
 - WritePrivateProfileStructA
 - winbase/WritePrivateProfileStructA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - WritePrivateProfileStruct
 - WritePrivateProfileStructA
 - WritePrivateProfileStructW
---

# WritePrivateProfileStructA function


## -description

Copies data into a key in the specified section of an initialization file. As it copies the data, the function calculates a checksum and appends it to the end of the data. The 
<a href="/windows/desktop/api/winbase/nf-winbase-getprivateprofilestruct">GetPrivateProfileStruct</a> function uses the checksum to ensure the integrity of the data.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpszSection [in]

The name of the section to which the string will be copied. If the section does not exist, it is created. The name of the section is case independent, the string can be any combination of uppercase and lowercase letters.

### -param lpszKey [in]

The name of the key to be associated with a string. If the key does not exist in the specified section, it is created. If this parameter is <b>NULL</b>, the entire section, including all keys and entries within the section, is deleted.

### -param lpStruct [in]

The data to be copied. If this parameter is <b>NULL</b>, the key is deleted.

### -param uSizeStruct [in]

The size of the buffer pointed to by the <i>lpStruct</i> parameter, in bytes.

### -param szFile [in]

The  name of the initialization file. If this parameter is <b>NULL</b>, the information is copied into the Win.ini file.

If the file was created using Unicode characters, the function writes Unicode characters to the file. Otherwise, the function writes ANSI characters.

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

If the <i>szFile</i> parameter does not contain a full path and file name for the file, 
<a href="/windows/desktop/api/winbase/nf-winbase-writeprivateprofilestringa">WritePrivateProfileString</a> searches the Windows directory for the file. If the file does not exist, this function creates the file in the Windows directory.

If <i>szFile</i> contains a full path and file name and the file does not exist, 
<a href="/windows/desktop/api/winbase/nf-winbase-writeprofilestringa">WriteProfileString</a> creates the file. The specified directory must already exist.

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




> [!NOTE]
> The winbase.h header defines WritePrivateProfileStruct as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprivateprofilestring">GetPrivateProfileString</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeprofilestringa">WriteProfileString</a>
