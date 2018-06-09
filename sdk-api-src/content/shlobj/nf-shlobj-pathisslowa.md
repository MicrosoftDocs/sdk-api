---
UID: NF:shlobj.PathIsSlowA
title: PathIsSlowA function
author: windows-sdk-content
description: PathIsSlow may be altered or unavailable.
old-location: shell\PathIsSlow.htm
old-project: shell
ms.assetid: f848a098-9248-453b-a957-77c35d70e528
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: PathIsSlow, PathIsSlow function [Windows Shell], PathIsSlowA, PathIsSlowW, _win32_PathIsSlow, shell.PathIsSlow, shlobj/PathIsSlow, shlobj/PathIsSlowA, shlobj/PathIsSlowW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: AUTOCOMPLETEOPTIONS
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
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 5.0
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

TBD




#### - dwFileAttr

Type: <b>DWORD</b>

The file attributes, if known; otherwise, pass –1 and this function gets the attributes by calling <a href="https://msdn.microsoft.com/9f9bcdbb-1ffd-49c2-92f4-181fdcc9c690">GetFileAttributes</a>. See <b>GetFileAttributes</b> for a list of file attributes.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the connection is high-latency; otherwise, <b>FALSE</b>.




## -remarks



A path is considered slow if the MultinetGetConnectionPerformance function returns a dwSpeed of 400 or less in its <a href="https://msdn.microsoft.com/977c717d-7624-46ab-b17d-25f42ef68be8">NETCONNECTINFOSTRUCT</a> structure—this is the speed of the media to the network resource, in 100 bits-per-second (bps)—or if FILE_ATTRIBUTE_OFFLINE is set on the file.

Note that network conditions can impact function performance time.



