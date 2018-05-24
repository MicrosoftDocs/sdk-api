---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.GetVideoProcessorCaps
title: ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps
author: windows-driver-content
description: Gets the capabilities of the video processor.
old-location: mf\id3d11videoprocessorenumerator_getvideoprocessorcaps.htm
old-project: medfound
ms.assetid: BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetVideoProcessorCaps, GetVideoProcessorCaps method [Media Foundation], GetVideoProcessorCaps method [Media Foundation],ID3D11VideoProcessorEnumerator interface, ID3D11VideoProcessorEnumerator interface [Media Foundation],GetVideoProcessorCaps method, ID3D11VideoProcessorEnumerator.GetVideoProcessorCaps, ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps, d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps, mf.id3d11videoprocessorenumerator_getvideoprocessorcaps
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
-	ID3D11VideoProcessorEnumerator.GetVideoProcessorCaps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps


## -description


Gets the capabilities of the video processor.


## -parameters




### -param pCaps [out]

A pointer to a <a href="https://msdn.microsoft.com/EF79BE15-B92E-45C1-BC42-E89E06197C20">D3D11_VIDEO_PROCESSOR_CAPS</a> structure that receives the capabilities.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8713B4C6-B08E-4616-92A7-05280CCE7AB3">ID3D11VideoProcessorEnumerator</a>
 

 

