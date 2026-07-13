---
UID: NF:winbase.GetPrivateProfileSectionNamesW
title: GetPrivateProfileSectionNamesW function (winbase.h)
description: The GetPrivateProfileSectionNamesW (Unicode) function (winbase.h) retrieves the names of all sections in an initialization file.
helpviewer_keywords: ["GetPrivateProfileSectionNames", "GetPrivateProfileSectionNames function", "GetPrivateProfileSectionNamesW", "_win32_getprivateprofilesectionnames", "base.getprivateprofilesectionnames", "winbase/GetPrivateProfileSectionNames", "winbase/GetPrivateProfileSectionNamesW"]
old-location: base\getprivateprofilesectionnames.htm
tech.root: winprog
ms.assetid: f5d8593d-d086-4a28-b067-be3806ba78c3
ms.date: 08/04/2022
ms.keywords: GetPrivateProfileSectionNames, GetPrivateProfileSectionNames function, GetPrivateProfileSectionNamesA, GetPrivateProfileSectionNamesW, _win32_getprivateprofilesectionnames, base.getprivateprofilesectionnames, winbase/GetPrivateProfileSectionNames, winbase/GetPrivateProfileSectionNamesA, winbase/GetPrivateProfileSectionNamesW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetPrivateProfileSectionNamesW (Unicode) and GetPrivateProfileSectionNamesA (ANSI)
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
 - GetPrivateProfileSectionNamesW
 - winbase/GetPrivateProfileSectionNamesW
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
 - GetPrivateProfileSectionNames
 - GetPrivateProfileSectionNamesA
 - GetPrivateProfileSectionNamesW
---

# GetPrivateProfileSectionNamesW function


## -description

Retrieves the names of all sections in an initialization file.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit Windows-based applications. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpszReturnBuffer [out]

A pointer to a buffer that receives the section names associated with the named file. The buffer is filled with one or more <b>null</b>-terminated strings; the last string is followed by a second <b>null</b> character.

### -param nSize [in]

The size of the buffer pointed to by the <i>lpszReturnBuffer</i> parameter, in characters.

### -param lpFileName [in]

The name of the initialization file. If this parameter is <b>NULL</b>, the function searches the Win.ini file. If this parameter does not contain a full path to the file, the system searches for the file in the Windows directory.

## -returns

The return value specifies the number of characters copied to the specified buffer, not including the terminating <b>null</b> character. If the buffer is not large enough to contain all the section names associated with the specified initialization file, the return value is equal to the size specified by <i>nSize</i> minus two.

## -remarks

This operation is atomic; no updates to the initialization file are allowed while the section names are being copied to the buffer.

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
> The winbase.h header defines GetPrivateProfileSectionNames as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection">GetPrivateProfileSection</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeprivateprofilesectiona">WritePrivateProfileSection</a>
