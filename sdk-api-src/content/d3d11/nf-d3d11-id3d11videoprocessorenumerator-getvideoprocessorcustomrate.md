---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.GetVideoProcessorCustomRate
title: ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate method
author: windows-driver-content
description: Gets a list of custom frame rates that a video processor supports.
old-location: mf\id3d11videoprocessorenumerator_getvideoprocessorcustomrate.htm
old-project: medfound
ms.assetid: 0FA868E6-B0FB-433B-A183-72DDE39B207E
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetVideoProcessorCustomRate method [Media Foundation], GetVideoProcessorCustomRate method [Media Foundation], ID3D11VideoProcessorEnumerator interface, GetVideoProcessorCustomRate,ID3D11VideoProcessorEnumerator.GetVideoProcessorCustomRate, ID3D11VideoProcessorEnumerator, ID3D11VideoProcessorEnumerator interface [Media Foundation], GetVideoProcessorCustomRate method, ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate, d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate, mf.id3d11videoprocessorenumerator_getvideoprocessorcustomrate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.h
api_name:
-	ID3D11VideoProcessorEnumerator.GetVideoProcessorCustomRate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate method


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
 

 

