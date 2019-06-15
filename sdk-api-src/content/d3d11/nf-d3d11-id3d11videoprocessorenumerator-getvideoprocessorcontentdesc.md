---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.GetVideoProcessorContentDesc
title: ID3D11VideoProcessorEnumerator::GetVideoProcessorContentDesc (d3d11.h)
author: windows-sdk-content
description: Gets the content description that was used to create this enumerator.
old-location: mf\id3d11videoprocessorenumerator_getvideoprocessorcontentdesc.htm
tech.root: medfound
ms.assetid: BDB52B2E-1D76-4867-AD58-2A77BC5B6ABD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorContentDesc, GetVideoProcessorContentDesc method [Media Foundation], GetVideoProcessorContentDesc method [Media Foundation],ID3D11VideoProcessorEnumerator interface, ID3D11VideoProcessorEnumerator interface [Media Foundation],GetVideoProcessorContentDesc method, ID3D11VideoProcessorEnumerator.GetVideoProcessorContentDesc, ID3D11VideoProcessorEnumerator::GetVideoProcessorContentDesc, d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorContentDesc, mf.id3d11videoprocessorenumerator_getvideoprocessorcontentdesc
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoProcessorEnumerator.GetVideoProcessorContentDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoProcessorEnumerator::GetVideoProcessorContentDesc


## -description


Gets the content description that was used to create this enumerator.


## -parameters




### -param pContentDesc [out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_content_desc">D3D11_VIDEO_PROCESSOR_CONTENT_DESC</a> structure that receives the content description.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a>
 

 

