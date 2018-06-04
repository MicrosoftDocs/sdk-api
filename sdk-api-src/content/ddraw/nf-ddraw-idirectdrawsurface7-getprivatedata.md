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

# IDirectDrawSurface7::GetPrivateData


## -description


Copies the private data that is associated with this surface to a provided buffer.


## -parameters




### -param






#### - guidTag [in]

Reference to (C++) or address of (C) the globally unique identifier that identifies the private data to be retrieved.


#### - lpBuffer [out]

A pointer to a previously allocated buffer that receives the requested private data if the call succeeds. The application that calls this method must allocate and release this buffer.


#### - lpcbBufferSize [in, out]

A pointer to a variable that contains the size value of the buffer at <i>lpBuffer</i>, in bytes. If this value is less than the actual size of the private data (such as 0), <b>GetPrivateData</b> sets the variable to the required buffer size, and then returns DDERR_MOREDATA.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_EXPIRED</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_MOREDATA</li>
<li>DDERR_NOTFOUND</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetPrivateData</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

