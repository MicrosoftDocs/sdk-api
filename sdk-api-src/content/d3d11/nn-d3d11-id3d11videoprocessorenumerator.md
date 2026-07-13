---
UID: NN:d3d11.ID3D11VideoProcessorEnumerator
title: ID3D11VideoProcessorEnumerator (d3d11.h)
description: Enumerates the video processor capabilities of a Microsoft Direct3D 11 device. (ID3D11VideoProcessorEnumerator)
helpviewer_keywords: ["ID3D11VideoProcessorEnumerator","ID3D11VideoProcessorEnumerator interface [Media Foundation]","ID3D11VideoProcessorEnumerator interface [Media Foundation]","described","d3d11/ID3D11VideoProcessorEnumerator","mf.id3d11videoprocessorenumerator"]
old-location: mf\id3d11videoprocessorenumerator.htm
tech.root: mf
ms.assetid: 8713B4C6-B08E-4616-92A7-05280CCE7AB3
ms.date: 12/05/2018
ms.keywords: ID3D11VideoProcessorEnumerator, ID3D11VideoProcessorEnumerator interface [Media Foundation], ID3D11VideoProcessorEnumerator interface [Media Foundation],described, d3d11/ID3D11VideoProcessorEnumerator, mf.id3d11videoprocessorenumerator
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoProcessorEnumerator
 - d3d11/ID3D11VideoProcessorEnumerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoProcessorEnumerator
---

# ID3D11VideoProcessorEnumerator interface


## -description

Enumerates the video processor capabilities of a Microsoft Direct3D 11 device.

## -inheritance

The <b>ID3D11VideoProcessorEnumerator</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11VideoProcessorEnumerator</b> also has these types of members:

## -remarks

To get a pointer to this interface, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>.

To create an instance of the video processor, pass the <b>ID3D11VideoProcessorEnumerator</b> pointer to the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a> method.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videoprocessorenumerator1">ID3D11VideoProcessorEnumerator</a>
