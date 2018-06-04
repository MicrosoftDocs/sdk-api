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

# IDirectDrawSurface7::BltBatch


## -description


The <b>IDirectDrawSurface7::BltBatch</b> method is not currently implemented.




## -parameters




### -param






#### - dwCount [in]

Number of bitblt operations to be performed.


#### - dwFlags [in]

Currently not used and must be set to 0.


#### - lpDDBltBatch [in]

A pointer to the first <a href="https://msdn.microsoft.com/d8c302aa-9c57-41f8-ad22-d8fdd1158c3c">DDBLTBATCH</a> structure that defines the parameters for the bitblt operations.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDCLIPLIST</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_INVALIDRECT</li>
<li>DDERR_NOALPHAHW</li>
<li>DDERR_NOBLTHW</li>
<li>DDERR_NOCLIPLIST</li>
<li>DDERR_NODDROPSHW</li>
<li>DDERR_NOMIRRORHW</li>
<li>DDERR_NORASTEROPHW</li>
<li>DDERR_NOROTATIONHW</li>
<li>DDERR_NOSTRETCHHW</li>
<li>DDERR_NOZBUFFERHW</li>
<li>DDERR_SURFACEBUSY</li>
<li>DDERR_SURFACELOST</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>BltBatch</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

