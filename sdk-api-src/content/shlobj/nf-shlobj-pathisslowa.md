---
UID: NF:shlobj.PathIsSlowA
title: PathIsSlowA function (shlobj.h)
description: PathIsSlow may be altered or unavailable. (ANSI)
helpviewer_keywords: ["PathIsSlowA", "shlobj/PathIsSlowA"]
old-location: shell\PathIsSlow.htm
tech.root: shell
ms.assetid: f848a098-9248-453b-a957-77c35d70e528
ms.date: 12/05/2018
ms.keywords: PathIsSlow, PathIsSlow function [Windows Shell], PathIsSlowA, PathIsSlowW, _win32_PathIsSlow, shell.PathIsSlow, shlobj/PathIsSlow, shlobj/PathIsSlowA, shlobj/PathIsSlowW
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathIsSlowW (Unicode) and PathIsSlowA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PathIsSlowA
 - shlobj/PathIsSlowA
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
 - PathIsSlow
 - PathIsSlowA
 - PathIsSlowW
---

# PathIsSlowA function


## -description

<p class="CCE_Message">[<b>PathIsSlow</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Determines whether a file path is a high-latency network connection.

## -parameters

### -param pszFile [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the fully qualified path of the file.

### -param dwAttr

Type: <b>DWORD</b>

The file attributes, if known; otherwise, pass –1 and this function gets the attributes by calling <a href="/windows/desktop/api/fileapi/nf-fileapi-getfileattributesa">GetFileAttributes</a>. See <b>GetFileAttributes</b> for a list of file attributes.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if the connection is high-latency; otherwise, <b>FALSE</b>.

## -remarks

A path is considered slow if the MultinetGetConnectionPerformance function returns a dwSpeed of 400 or less in its <a href="/windows/desktop/api/winnetwk/ns-winnetwk-netconnectinfostruct">NETCONNECTINFOSTRUCT</a> structure—this is the speed of the media to the network resource, in 100 bits-per-second (bps)—or if FILE_ATTRIBUTE_OFFLINE is set on the file.

Note that network conditions can impact function performance time.




> [!NOTE]
> The shlobj.h header defines PathIsSlow as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
