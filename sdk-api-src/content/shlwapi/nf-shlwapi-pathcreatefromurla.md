---
UID: NF:shlwapi.PathCreateFromUrlA
title: PathCreateFromUrlA function
author: windows-driver-content
description: Converts a file URL to a Microsoft MS-DOS path.
old-location: shell\PathCreateFromUrl.htm
old-project: shell
ms.assetid: f4136c80-a309-4551-be73-f2f24ecd4675
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: PathCreateFromUrl, PathCreateFromUrl function [Windows Shell], PathCreateFromUrlA, PathCreateFromUrlW, _win32_PathCreateFromUrl, shell.PathCreateFromUrl, shlwapi/PathCreateFromUrl, shlwapi/PathCreateFromUrlA, shlwapi/PathCreateFromUrlW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: PathCreateFromUrlW (Unicode) and PathCreateFromUrlA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: URL_SCHEME
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Shlwapi.dll
-	API-MS-Win-Core-url-l1-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-0.dll
-	API-MS-Win-DownLevel-shlwapi-l1-1-1.dll
api_name:
-	PathCreateFromUrl
-	PathCreateFromUrlA
-	PathCreateFromUrlW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# PathCreateFromUrlA function


## -description


Converts a file URL to a Microsoft MS-DOS path.


## -parameters




### -param pszUrl [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.


### -param pszPath [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the MS-DOS path. You must set the size of this buffer to MAX_PATH to ensure that it is large enough to hold the returned string.


### -param pcchPath [in, out]

Type: <b>DWORD*</b>

The number of characters in the <i>pszPath</i> buffer.


### -param dwFlags

Type: <b>DWORD</b>

Reserved. Set this parameter to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



