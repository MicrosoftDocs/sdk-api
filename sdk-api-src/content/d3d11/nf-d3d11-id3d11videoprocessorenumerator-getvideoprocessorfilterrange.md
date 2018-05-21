---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.GetVideoProcessorFilterRange
title: ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange
author: windows-driver-content
description: Gets the range of values for an image filter.
old-location: mf\id3d11videoprocessorenumerator_getvideoprocessorfilterrange.htm
old-project: medfound
ms.assetid: F43A01D7-A0FE-4509-B3B2-094B09A7F04A
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: GetVideoProcessorFilterRange, GetVideoProcessorFilterRange method [Media Foundation], GetVideoProcessorFilterRange method [Media Foundation],ID3D11VideoProcessorEnumerator interface, ID3D11VideoProcessorEnumerator interface [Media Foundation],GetVideoProcessorFilterRange method, ID3D11VideoProcessorEnumerator.GetVideoProcessorFilterRange, ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange, d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange, mf.id3d11videoprocessorenumerator_getvideoprocessorfilterrange
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
-	ID3D11VideoProcessorEnumerator.GetVideoProcessorFilterRange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoProcessorEnumerator::GetVideoProcessorFilterRange


## -description


Gets the range of values for an image filter.


## -parameters




### -param Filter [in]

The type of image filter, specified as a <a href="https://msdn.microsoft.com/87CF9A1A-E196-4B5A-BAAE-DD948A5468C2">D3D11_VIDEO_PROCESSOR_FILTER</a> value.


### -param pRange [out]

A pointer to a <a href="https://msdn.microsoft.com/22B11763-717A-49D7-8F5B-2FD21C13F11E">D3D11_VIDEO_PROCESSOR_FILTER_RANGE</a> structure. The method fills the structure with the range of values for the specified filter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/8713B4C6-B08E-4616-92A7-05280CCE7AB3">ID3D11VideoProcessorEnumerator</a>
 

 

