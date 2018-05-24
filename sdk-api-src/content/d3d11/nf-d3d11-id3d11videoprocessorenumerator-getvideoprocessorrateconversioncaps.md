---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.GetVideoProcessorRateConversionCaps
title: ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps
author: windows-driver-content
description: Returns a group of video processor capabilities that are associated with frame-rate conversion, including deinterlacing and inverse telecine.
old-location: mf\id3d11videoprocessorenumerator_getvideoprocessorrateconversioncaps.htm
old-project: medfound
ms.assetid: 2DB74CB9-C6B3-477A-9EF9-6E2EC1DE37D6
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetVideoProcessorRateConversionCaps, GetVideoProcessorRateConversionCaps method [Media Foundation], GetVideoProcessorRateConversionCaps method [Media Foundation],ID3D11VideoProcessorEnumerator interface, ID3D11VideoProcessorEnumerator interface [Media Foundation],GetVideoProcessorRateConversionCaps method, ID3D11VideoProcessorEnumerator.GetVideoProcessorRateConversionCaps, ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps, d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps, mf.id3d11videoprocessorenumerator_getvideoprocessorrateconversioncaps
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
-	ID3D11VideoProcessorEnumerator.GetVideoProcessorRateConversionCaps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

