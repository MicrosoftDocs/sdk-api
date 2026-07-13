---
UID: NF:winbase.GetProfileSectionA
title: GetProfileSectionA function (winbase.h)
description: Retrieves all the keys and values for the specified section of the Win.ini file. (ANSI)
helpviewer_keywords: ["GetProfileSectionA", "winbase/GetProfileSectionA"]
old-location: base\getprofilesection.htm
tech.root: winprog
ms.assetid: cc90811b-5e7b-4c75-987b-57f36a9408c5
ms.date: 12/05/2018
ms.keywords: GetProfileSection, GetProfileSection function, GetProfileSectionA, GetProfileSectionW, _win32_getprofilesection, base.getprofilesection, winbase/GetProfileSection, winbase/GetProfileSectionA, winbase/GetProfileSectionW
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetProfileSectionW (Unicode) and GetProfileSectionA (ANSI)
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
 - GetProfileSectionA
 - winbase/GetProfileSectionA
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
 - GetProfileSection
 - GetProfileSectionA
 - GetProfileSectionW
---

# GetProfileSectionA function


## -description

Retrieves all the keys and values for the specified section of the Win.ini file.
<div class="alert"><b>Note</b>  This function is provided only for compatibility with 16-bit Windows-based applications. Applications should store initialization information in the registry.</div><div> </div>

## -parameters

### -param lpAppName [in]

The name of the section in the Win.ini file.

### -param lpReturnedString [out]

A pointer to a buffer that receives the keys and values associated with the named section. The buffer is filled with one or more null-terminated strings; the last string is followed by a second null character.

### -param nSize [in]

The size of the buffer pointed to by the <i>lpReturnedString</i> parameter, in characters. 


 


The maximum profile section size is 32,767 characters.

## -returns

The return value specifies the number of characters copied to the specified buffer, not including the terminating null character. If the buffer is not large enough to contain all the keys and values associated with the named section, the return value is equal to the size specified by <i>nSize</i> minus two.

## -remarks

The format of the returned keys and values is one or more null-terminated strings, followed by a final null character. Each string has the following form: <i>key</i>=<i>string</i>

The 
<b>GetProfileSection</b> function is not case-sensitive; the strings can be a combination of uppercase and lowercase letters.

This operation is atomic; no updates to the Win.ini file are allowed while the keys and values for the section are being copied to the buffer.

<b>Windows Server 2003 and Windows XP/2000:  </b>Calls to profile functions may be mapped to the registry instead of to the initialization files. This mapping occurs when the initialization file and section are specified in the registry under the following key: <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\IniFileMapping</b>.

When the operation has been mapped, the 
<b>GetProfileSection</b> function retrieves information from the registry, not from the initialization file; the change in the storage location has no effect on the function's behavior.

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
> The winbase.h header defines GetProfileSection as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getprivateprofilesection">GetPrivateProfileSection</a>



<a href="/windows/desktop/api/winbase/nf-winbase-writeprofilesectiona">WriteProfileSection</a>
