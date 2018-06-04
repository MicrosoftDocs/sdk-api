---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# UrlHashW function


## -description


Hashes a URL string.


## -parameters




### -param pszUrl

TBD


### -param pbHash [out]

Type: <b>BYTE*</b>

A pointere to a buffer that, when this function returns successfully, receives the hashed array.


### -param cbHash

Type: <b>DWORD</b>

The number of elements in the array at <i>pbHash</i>. It should be no larger than 256.


#### - pszURL [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the URL.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To hash a URL into a single byte, set <i>cbHash</i> = sizeof(BYTE) and <i>pbHash</i> = (LPBYTE)&amp;bHashedValue, where bHashedValue is a one-byte buffer. To hash a URL into a <b>DWORD</b>, set <i>cbHash</i> = sizeof(DWORD) and <i>pbHash</i> = (LPBYTE)&amp;dwHashedValue, where dwHashedValue is a <b>DWORD</b> buffer.




## -see-also




<a href="https://msdn.microsoft.com/7b42b3ae-c021-49be-b5a7-d3bc0a5d346a">HashData</a>
 

 

