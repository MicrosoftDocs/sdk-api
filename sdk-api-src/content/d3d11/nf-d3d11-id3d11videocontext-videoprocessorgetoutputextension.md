---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputExtension
title: ID3D11VideoContext::VideoProcessorGetOutputExtension (d3d11.h)
description: Gets private state data from the video processor.helpviewer_keywords: ["ID3D11VideoContext interface [Media Foundation]","VideoProcessorGetOutputExtension method","ID3D11VideoContext.VideoProcessorGetOutputExtension","ID3D11VideoContext::VideoProcessorGetOutputExtension","VideoProcessorGetOutputExtension","VideoProcessorGetOutputExtension method [Media Foundation]","VideoProcessorGetOutputExtension method [Media Foundation]","ID3D11VideoContext interface","d3d11/ID3D11VideoContext::VideoProcessorGetOutputExtension","mf.id3d11videocontext_videoprocessorgetoutputextension"]
old-location: mf\id3d11videocontext_videoprocessorgetoutputextension.htm
tech.root: medfound
ms.assetid: 3B979D5D-CB3D-4B67-9BE3-277005076604
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorGetOutputExtension method, ID3D11VideoContext.VideoProcessorGetOutputExtension, ID3D11VideoContext::VideoProcessorGetOutputExtension, VideoProcessorGetOutputExtension, VideoProcessorGetOutputExtension method [Media Foundation], VideoProcessorGetOutputExtension method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorGetOutputExtension, mf.id3d11videocontext_videoprocessorgetoutputextension
f1_keywords:
- d3d11/ID3D11VideoContext.VideoProcessorGetOutputExtension
dev_langs:
- c++
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
- ID3D11VideoContext.VideoProcessorGetOutputExtension
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::VideoProcessorGetOutputExtension


## -description


Gets private state data from the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessor">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessor">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param pExtensionGuid [in]

A pointer to a GUID that identifies the state. The meaning of this GUID is defined by the graphics driver.


### -param DataSize [in]

The size of the <i>pData</i> buffer, in bytes.


### -param pData [out]

A pointer to a buffer that receives the private state data. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

