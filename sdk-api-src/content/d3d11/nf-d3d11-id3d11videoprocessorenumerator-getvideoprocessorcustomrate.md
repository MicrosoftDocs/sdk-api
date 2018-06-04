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

# ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate


## -description


Gets a list of custom frame rates that a video processor supports.


## -parameters




### -param TypeIndex [in]

The zero-based index of the frame-rate capability group. To get the maxmum index, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps </a> and check the <b>RateConversionCapsCount</b> member of the <a href="https://msdn.microsoft.com/EF79BE15-B92E-45C1-BC42-E89E06197C20">D3D11_VIDEO_PROCESSOR_CAPS</a> structure.


### -param CustomRateIndex [in]

The zero-based index of the custom rate to retrieve. To get the maximum index, call <a href="https://msdn.microsoft.com/2DB74CB9-C6B3-477A-9EF9-6E2EC1DE37D6">ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps</a> and check the <b>CustomRateCount</b> member of the <a href="https://msdn.microsoft.com/C8C50AE4-5F4F-42AB-8FBB-37D24C4D6081">D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS</a> structure.

This index value is always relative to the capability group specified in the <i>TypeIndex</i> parameter.


### -param pRate [out]

A pointer to a <a href="https://msdn.microsoft.com/237357C8-546E-41E5-8002-E5499E39DA72">D3D11_VIDEO_PROCESSOR_CUSTOM_RATE</a> structure that receives the custom rate.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8713B4C6-B08E-4616-92A7-05280CCE7AB3">ID3D11VideoProcessorEnumerator</a>
 

 

