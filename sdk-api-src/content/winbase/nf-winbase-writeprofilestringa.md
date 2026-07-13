---
UID: NF:winbase.WriteProfileStringA
title: WriteProfileStringA function (winbase.h)
description: Copies a string into the specified section of the Win.ini file. (ANSI)
helpviewer_keywords: ["WriteProfileStringA", "winbase/WriteProfileStringA"]
old-location: base\writeprofilestring.htm
tech.root: winprog
ms.assetid: d3fb74bb-7ce9-4669-8f00-02ac8a95ddd5
ms.date: 12/05/2018
ms.keywords: WriteProfileString, WriteProfileString function, WriteProfileStringA, WriteProfileStringW, _win32_writeprofilestring, base.writeprofilestring, winbase/WriteProfileString, winbase/WriteProfileStringA, winbase/WriteProfileStringW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WriteProfileStringW (Unicode) and WriteProfileStringA (ANSI)
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
 - WriteProfileStringA
 - winbase/WriteProfileStringA
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
 - WriteProfileString
 - WriteProfileStringA
 - WriteProfileStringW
---

# WriteProfileStringA function


## -description

Copies a string into the specified section of the Win.ini file. If Win.ini uses Unicode characters, the function writes Unicode characters to the file. Otherwise, the function writes ANSI characters.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpAppName [in]

The section to which the string is to be copied. If the section does not exist, it is created. The name of the section is not case-sensitive; the string can be any combination of uppercase and lowercase letters.

### -param lpKeyName [in]

The key to be associated with the string. If the key does not exist in the specified section, it is created. If this parameter is <b>NULL</b>, the entire section, including all entries in the section, is deleted.

### -param lpString [in]

A <b>null</b>-terminated string to be written to the file. If this parameter is <b>NULL</b>, the key pointed to by the <i>lpKeyName</i> parameter is deleted.

## -returns

If the function successfully copies the string to the Win.ini file, the return value is nonzero.

If the function fails, or if it flushes the cached version of Win.ini, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

A section in the Win.ini file must have the following form: <i>key</i>=<i>string</i>.

The system keeps a cached version of the most recent registry file mapping to improve performance. If all parameters are <b>NULL</b>, the function flushes the cache. While the system is editing the cached version of the file, processes that edit the file itself will use the original file until the cache has been cleared.

The system maps most .ini file references to the registry, using the mapping defined under the following registry key: <pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>IniFileMapping</b></pre>


When the operation has been mapped, the 
<b>WriteProfileString</b> function writes information to the registry, not to the initialization file; the change in the storage location has no effect on the function's behavior.

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
> The winbase.h header defines WriteProfileString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprofilestringa">GetProfileString</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeprivateprofilestringa">WritePrivateProfileString</a>
