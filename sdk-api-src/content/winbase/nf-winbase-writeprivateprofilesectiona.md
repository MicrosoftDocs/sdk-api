---
UID: NF:winbase.WritePrivateProfileSectionA
title: WritePrivateProfileSectionA function (winbase.h)
description: Replaces the keys and values for the specified section in an initialization file. (ANSI)
helpviewer_keywords: ["WritePrivateProfileSectionA", "winbase/WritePrivateProfileSectionA"]
old-location: base\writeprivateprofilesection.htm
tech.root: winprog
ms.assetid: 23f9e012-4196-437a-9e22-0524b37505b4
ms.date: 12/05/2018
ms.keywords: WritePrivateProfileSection, WritePrivateProfileSection function, WritePrivateProfileSectionA, WritePrivateProfileSectionW, _win32_writeprivateprofilesection, base.writeprivateprofilesection, winbase/WritePrivateProfileSection, winbase/WritePrivateProfileSectionA, winbase/WritePrivateProfileSectionW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WritePrivateProfileSectionW (Unicode) and WritePrivateProfileSectionA (ANSI)
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
 - WritePrivateProfileSectionA
 - winbase/WritePrivateProfileSectionA
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
 - WritePrivateProfileSection
 - WritePrivateProfileSectionA
 - WritePrivateProfileSectionW
---

# WritePrivateProfileSectionA function


## -description

Replaces the keys and values for the specified section in an initialization file.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpAppName [in]

The name of the section in which data is written. This section name is typically the name of the calling application.

### -param lpString [in]

The new key names and associated values that are to be written to the named section. This string is limited to 65,535 bytes.

### -param lpFileName [in]

The name of the initialization file. If this parameter does not contain a full path for the file, the function searches the Windows directory for the file. If the file does not exist and <i>lpFileName</i> does not contain a full path, the function creates the file in the Windows directory. 

If the file exists and was created using Unicode characters, the function writes Unicode characters to the file. Otherwise, the function creates a file using ANSI characters.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The data in the buffer pointed to by the <i>lpString</i> parameter consists of one or more <b>null</b>-terminated strings, followed by a final <b>null</b> character. Each string has the following form:

<i>key</i><b>=</b><i>string</i>

The 
<b>WritePrivateProfileSection</b> function is not case-sensitive; the string pointed to by the <i>lpAppName</i> parameter can be a combination of uppercase and lowercase letters.

If no section name matches the string pointed to by the <i>lpAppName</i> parameter, 
<b>WritePrivateProfileSection</b> creates the section at the end of the specified initialization file and initializes the new section with the specified key name and value pairs.

<b>WritePrivateProfileSection</b> deletes the existing keys and values for the named section and inserts the key names and values in the buffer pointed to by the <i>lpString</i> parameter. The function does not attempt to correlate old and new key names; if the new names appear in a different order from the old names, any comments associated with preexisting keys and values in the initialization file will probably be associated with incorrect keys and values.

This operation is atomic; no operations that read from or write to the specified initialization file are allowed while the information is being written.

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
> The winbase.h header defines WritePrivateProfileSection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection">GetPrivateProfileSection</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa">RegCreateKeyEx</a>



<a href="/windows/desktop/api/winreg/nf-winreg-regsetvalueexa">RegSetValueEx</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeprofilesectiona">WriteProfileSection</a>
