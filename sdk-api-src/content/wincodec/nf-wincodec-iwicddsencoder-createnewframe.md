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

# IWICDdsEncoder::CreateNewFrame


## -description


Creates a new frame to encode.


## -parameters




### -param ppIFrameEncode [out]

A pointer to the newly created frame object.


### -param pArrayIndex [out, optional]

Points to the location where the array index is returned.


### -param pMipLevel [out, optional]

Points to the location where the mip level index is returned.


### -param pSliceIndex [out, optional]

Points to the location where the slice index is returned.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is equivalent to <a href="https://msdn.microsoft.com/1c48f603-e7be-4b0c-a262-0dd01308e868">IWICBitmapEncoder::CreateNewFrame</a>, but returns additional information about the array index, mip level and slice of the newly created frame. In contrast to <b>IWICBitmapEncoder::CreateNewFrame</b>, there is no <a href="https://msdn.microsoft.com/b97caba6-298a-4b36-9f39-9b5440b866c3">IPropertyBag2</a>* parameter because individual DDS frames do not have separate properties.




## -see-also




<a href="https://msdn.microsoft.com/DF14309F-7595-4ABE-BB6E-03D2914CC86D">IWICDdsEncoder</a>



<a href="https://msdn.microsoft.com/2E5755B4-E8DC-40B2-8DA1-B053A261079B">WICDdsParameters</a>
 

 

