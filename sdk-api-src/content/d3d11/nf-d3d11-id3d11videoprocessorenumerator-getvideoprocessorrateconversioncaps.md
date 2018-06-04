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

# ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps


## -description


Returns a group of video processor capabilities that are associated with frame-rate conversion, including deinterlacing and inverse telecine.


## -parameters




### -param TypeIndex [in]

The zero-based index of the group to retrieve. To get the maximum index, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>RateConversionCapsCount</b> member of the <a href="https://msdn.microsoft.com/EF79BE15-B92E-45C1-BC42-E89E06197C20">D3D11_VIDEO_PROCESSOR_CAPS</a> structure.


### -param pCaps [out]

A pointer to a <a href="https://msdn.microsoft.com/C8C50AE4-5F4F-42AB-8FBB-37D24C4D6081">D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS</a> structure that receives the frame-rate conversion capabilities.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The capabilities defined in the <a href="https://msdn.microsoft.com/C8C50AE4-5F4F-42AB-8FBB-37D24C4D6081">D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS</a> structure are interdependent. Therefore, the driver can support multiple, distinct groups of these capabilities. 




## -see-also




<a href="https://msdn.microsoft.com/8713B4C6-B08E-4616-92A7-05280CCE7AB3">ID3D11VideoProcessorEnumerator</a>
 

 

