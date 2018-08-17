---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamExtension
title: ID3D11VideoContext::VideoProcessorSetStreamExtension
author: windows-sdk-content
description: Sets a driver-specific state on a video processing stream.
old-location: mf\id3d11videocontext_videoprocessorsetstreamextension.htm
old-project: medfound
ms.assetid: E6E1CF26-6A9F-42E1-8DA7-2AC76CE05906
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamExtension method, ID3D11VideoContext.VideoProcessorSetStreamExtension, ID3D11VideoContext::VideoProcessorSetStreamExtension, VideoProcessorSetStreamExtension, VideoProcessorSetStreamExtension method [Media Foundation], VideoProcessorSetStreamExtension method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamExtension, mf.id3d11videocontext_videoprocessorsetstreamextension
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: d3d11.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.VideoProcessorSetStreamExtension
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::VideoProcessorSetStreamExtension


## -description


Sets a driver-specific state on a video processing stream.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/en-us/library/Hh447799(v=VS.85).aspx">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/en-us/library/Hh447788(v=VS.85).aspx">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/en-us/library/Hh447802(v=VS.85).aspx">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


### -param pExtensionGuid [in]

A pointer to a GUID that identifies the operation. The meaning of this GUID is defined by the graphics driver.


### -param DataSize [in]

The size of the <i>pData</i> buffer, in bytes.


### -param pData [in]

A pointer to a buffer that contains private state data. The method passes this buffer directly to the driver without validation. It is the responsibility of the driver to validate the data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh447703(v=VS.85).aspx">ID3D11VideoContext</a>
 

 

