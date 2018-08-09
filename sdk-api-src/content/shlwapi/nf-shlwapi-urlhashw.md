---
UID: NF:shlwapi.UrlHashW
title: UrlHashW function
author: windows-sdk-content
description: Hashes a URL string.
old-location: shell\UrlHash.htm
old-project: shell
ms.assetid: 9c0ce709-e097-4501-bee1-b24df9d4828d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UrlHash, UrlHash function [Windows Shell], UrlHashA, UrlHashW, _win32_UrlHash, shell.UrlHash, shlwapi/UrlHash, shlwapi/UrlHashA, shlwapi/UrlHashW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UrlHashW (Unicode) and UrlHashA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: URL_SCHEME
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-Core-url-l1-1-0.dll
 - KernelBase.dll
api_name:
 - UrlHash
 - UrlHashA
 - UrlHashW
product: Windows
targetos: Windows
req.lib: Shlwapi.lib
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
req.product: Internet Explorer 6.01
---

# UrlHashW function


## -description


Hashes a URL string.


## -parameters




### -param pszUrl [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.


### -param pbHash [out]

Type: <b>BYTE*</b>

A pointere to a buffer that, when this function returns successfully, receives the hashed array.


### -param cbHash

Type: <b>DWORD</b>

The number of elements in the array at <i>pbHash</i>. It should be no larger than 256.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To hash a URL into a single byte, set <i>cbHash</i> = sizeof(BYTE) and <i>pbHash</i> = (LPBYTE)&amp;bHashedValue, where bHashedValue is a one-byte buffer. To hash a URL into a <b>DWORD</b>, set <i>cbHash</i> = sizeof(DWORD) and <i>pbHash</i> = (LPBYTE)&amp;dwHashedValue, where dwHashedValue is a <b>DWORD</b> buffer.




## -see-also




<a href="https://msdn.microsoft.com/7b42b3ae-c021-49be-b5a7-d3bc0a5d346a">HashData</a>
 

 

