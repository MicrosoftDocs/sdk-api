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

# UrlCreateFromPathA function


## -description


Converts a Microsoft MS-DOS path to a canonicalized URL.


## -parameters




### -param pszPath [in]

Type: <b>PCTSTR</b>

A null-terminated string of maximum length INTERNET_MAX_URL_LENGTH that contains the MS-DOS path.


### -param pszUrl [out]

Type: <b>PTSTR</b>

A pointer to a buffer that, when this function returns successfully, receives the URL.


### -param pcchUrl [in, out]

Type: <b>DWORD*</b>

The number of characters in <i>pszUrl</i>.


### -param dwFlags

Type: <b>DWORD</b>

Reserved. Set this parameter to <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_FALSE if <i>pszPath</i> is already in URL format. In this case, <i>pszPath</i> will simply be copied to <i>pszUrl</i>. Otherwise, it returns S_OK if successful or a standard COM error value if not.




## -remarks



<div class="alert"><b>Note</b>  <b>UrlCreateFromPath</b> does not support extended paths. These are paths that include the extended-length path prefix "\\?\".</div>
<div> </div>


