---
UID: NF:shellapi.SHGetNewLinkInfoA
title: SHGetNewLinkInfoA function (shellapi.h)
description: Creates a name for a new shortcut based on the shortcut's proposed target. This function does not create the shortcut, just the name. (ANSI)
helpviewer_keywords: ["SHGNLI_NOLNK", "SHGNLI_NOLOCNAME", "SHGNLI_NOUNIQUE", "SHGNLI_PIDL", "SHGNLI_PREFIXNAME", "SHGNLI_USEURLEXT", "SHGetNewLinkInfoA", "shellapi/SHGetNewLinkInfoA"]
old-location: shell\SHGetNewLinkInfo.htm
tech.root: shell
ms.assetid: ca658d5c-af7b-400c-8f4d-7d4b07bf7f2b
ms.date: 12/05/2018
ms.keywords: SHGNLI_NOLNK, SHGNLI_NOLOCNAME, SHGNLI_NOUNIQUE, SHGNLI_PIDL, SHGNLI_PREFIXNAME, SHGNLI_USEURLEXT, SHGetNewLinkInfo, SHGetNewLinkInfo function [Windows Shell], SHGetNewLinkInfoA, SHGetNewLinkInfoW, _win32_SHGetNewLinkInfo, shell.SHGetNewLinkInfo, shellapi/SHGetNewLinkInfo, shellapi/SHGetNewLinkInfoA, shellapi/SHGetNewLinkInfoW
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHGetNewLinkInfoW (Unicode) and SHGetNewLinkInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHGetNewLinkInfoA
 - shellapi/SHGetNewLinkInfoA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetNewLinkInfo
 - SHGetNewLinkInfoA
 - SHGetNewLinkInfoW
---

# SHGetNewLinkInfoA function


## -description

Creates a name for a new shortcut based on the shortcut's proposed target. This function does not create the shortcut, just the name.

## -parameters

### -param pszLinkTo [in]

Type: <b>LPCTSTR</b>

A pointer to the path and file name of the shortcut's target. If <i>uFlags</i> does not contain the <b>SHGNLI_PIDL</b> value, this parameter is the address of a null-terminated string that contains the target. If <i>uFlags</i> contains the <b>SHGNLI_PIDL</b> value, this parameter is a PIDL that represents the target.

### -param pszDir [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the path of the folder in which the shortcut would be created.

### -param pszName [out]

Type: <b>LPTSTR</b>

A pointer to a string that receives the null-terminated path and file name for the shortcut. This buffer is assumed to be at least MAX_PATH characters in size.

### -param pfMustCopy [out]

Type: <b>BOOL*</b>

The address of a <b>BOOL</b> value that receives a flag indicating whether the shortcut would be copied. When a shortcut to another shortcut is created, the Shell simply copies the target shortcut and modifies that copied shortcut appropriately. This parameter receives a nonzero value if the target specified in <i>pszLinkTo</i> specifies a shortcut that will cause the target shortcut to be copied. This parameter receives zero if the target does not specify a shortcut that would be copied.

### -param uFlags [in]

Type: <b>UINT</b>

The options for the function. This can be zero or a combination of the following values.



#### SHGNLI_PIDL (0x000000001)

0x000000001. The target pointed to by <i>pszLinkTo</i> is a PIDL that represents the target. If this flag is not included, <i>pszLinkTo</i> is regarded as the address of a string that contains the path and file name of the target.



#### SHGNLI_NOUNIQUE (0x000000002)

0x000000002. Skip the normal checks that ensure that the shortcut name is unique within the destination folder. If this flag is not included, the function creates the shortcut name and then determines whether the name is unique in the destination folder. If a file with the same name already exists in the destination folder, the shortcut name will be modified. This process is repeated until a unique name is found.



#### SHGNLI_PREFIXNAME (0x000000004)

0x000000004. The created name will be preceded by the string "Shortcut to ".



#### SHGNLI_NOLNK (0x000000008)

0x000000008. <a href="/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)">Version 5.0</a> Do not add the .lnk file name extension. You must set the <b>_WIN32_IE</b> macro to 5.01 or greater to use this flag. For more information about versioning, see Shell and Common Controls Versions.



#### SHGNLI_NOLOCNAME (0x000000010)

0x000000010. <b>Windows Vista and later</b>. Use the non-localized parsing name of the target pointed to by <i>pszLinkTo</i> as the name of the shortcut file. If this flag is not set, the localized name is used.



#### SHGNLI_USEURLEXT (0x000000020)

0x000000020. <b>Windows 7 and later</b>. Append a .url file name extension (rather than .lnk) to the name pointed to by <i>pszName</i>. If this flag is not set, the shortcut name uses a .lnk extension unless SHGNLI_NOLNK is set.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful; otherwise, <b>FALSE</b>.

## -remarks

<b>SHGetNewLinkInfo</b> determines whether the destination file system supports long file names. If it does, a long file name is used for the shortcut name. If the destination file system does not support long file names, the shortcut name is returned in an 8.3 format.




> [!NOTE]
> The shellapi.h header defines SHGetNewLinkInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
