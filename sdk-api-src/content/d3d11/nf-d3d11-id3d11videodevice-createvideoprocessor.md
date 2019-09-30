---
UID: NF:d3d11.ID3D11VideoDevice.CreateVideoProcessor
title: ID3D11VideoDevice::CreateVideoProcessor (d3d11.h)
author: windows-sdk-content
description: Creates a video processor device for Microsoft Direct3D 11.
old-location: mf\id3d11videodevice_createvideoprocessor.htm
tech.root: medfound
ms.assetid: 5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateVideoProcessor, CreateVideoProcessor method [Media Foundation], CreateVideoProcessor method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateVideoProcessor method, ID3D11VideoDevice.CreateVideoProcessor, ID3D11VideoDevice::CreateVideoProcessor, d3d11/ID3D11VideoDevice::CreateVideoProcessor, mf.id3d11videodevice_createvideoprocessor
ms.topic: method
f1_keywords: 
 - "d3d11/ID3D11VideoDevice.CreateVideoProcessor"
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
 - ID3D11VideoDevice.CreateVideoProcessor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoDevice::CreateVideoProcessor


## -description


Creates a video processor device for Microsoft Direct3D 11.


## -parameters




### -param pEnum [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorenumerator">ID3D11VideoDevice::CreateVideoProcessorEnumerator</a>.


### -param RateConversionIndex [in]

Specifies the frame-rate conversion capabilities for the video processor. The value is a zero-based index that corresponds to the <i>TypeIndex</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorrateconversioncaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps</a> method. 


### -param ppVideoProcessor [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate">ID3D11DeviceContext::ClearState</a> method does not affect the internal state of the video processor.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videodevice">ID3D11VideoDevice</a>
 

 

