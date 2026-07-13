---
UID: NF:winbase.WriteProfileSectionW
title: WriteProfileSectionW function (winbase.h)
description: Replaces the contents of the specified section in the Win.ini file with specified keys and values. (Unicode)
helpviewer_keywords: ["WriteProfileSection", "WriteProfileSection function", "WriteProfileSectionW", "_win32_writeprofilesection", "base.writeprofilesection", "winbase/WriteProfileSection", "winbase/WriteProfileSectionW"]
old-location: base\writeprofilesection.htm
tech.root: winprog
ms.assetid: f712a7b4-d945-499c-b003-22204bc590d7
ms.date: 12/05/2018
ms.keywords: WriteProfileSection, WriteProfileSection function, WriteProfileSectionA, WriteProfileSectionW, _win32_writeprofilesection, base.writeprofilesection, winbase/WriteProfileSection, winbase/WriteProfileSectionA, winbase/WriteProfileSectionW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: WriteProfileSectionW (Unicode) and WriteProfileSectionA (ANSI)
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
 - WriteProfileSectionW
 - winbase/WriteProfileSectionW
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
 - WriteProfileSection
 - WriteProfileSectionA
 - WriteProfileSectionW
---

# WriteProfileSectionW function


## -description

Replaces the contents of the specified section in the Win.ini file with specified keys and values. If Win.ini uses Unicode characters, the function writes Unicode characters to the file. Otherwise, the function writes ANSI characters.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit versions of Windows. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpAppName [in]

The name of the section. This section name is typically the name of the calling application.

### -param lpString [in]

The new key names and associated values that are to be written to the named section. This string is limited to 65,535 bytes.

If the file exists and was created using Unicode characters, the function writes Unicode characters to the file. Otherwise, the function creates a file using ANSI characters.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Keys and values in the <i>lpString</i> buffer consist of one or more <b>null</b>-terminated strings, followed by a final <b>null</b> character. Each string has the following form: <i>key</i>=<i>string</i>.

The 
<b>WriteProfileSection</b> function is not case-sensitive; the strings can be a combination of uppercase and lowercase letters.

<b>WriteProfileSection</b> deletes the existing keys and values for the named section and inserts the key names and values in the buffer pointed to by <i>lpString</i>. The function does not attempt to correlate old and new key names; if the new names appear in a different order from the old names, any comments associated with preexisting keys and values in the initialization file will probably be associated with incorrect keys and values.

This operation is atomic; no other operations that read from or write to the initialization file are allowed while the information is being written.

The system keeps a cached version of the most recent registry file mapping to improve performance. If all parameters are <b>NULL</b>, the function flushes the cache. While the system is editing the cached version of the file, processes that edit the file itself will use the original file until the cache has been cleared.

The system maps most .ini file references to the registry, using the mapping defined under the following registry key: <pre><b>HKEY_LOCAL_MACHINE</b>
   <b>SOFTWARE</b>
      <b>Microsoft</b>
         <b>Windows NT</b>
            <b>CurrentVersion</b>
               <b>IniFileMapping</b></pre>


When the operation has been mapped, the 
<b>WriteProfileSection</b> function writes information to the registry, not to the initialization file; the change in the storage location has no effect on the function's behavior.

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
> The winbase.h header defines WriteProfileSection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprofilesectiona">GetProfileSection</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeprivateprofilesectiona">WritePrivateProfileSection</a>
