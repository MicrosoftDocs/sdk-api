---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetOutputExtension
title: ID3D11VideoContext::VideoProcessorSetOutputExtension
author: windows-sdk-content
description: Sets a driver-specific video processing state.
old-location: mf\id3d11videocontext_videoprocessorsetoutputextension.htm
tech.root: medfound
ms.assetid: 38279599-09C8-4BB1-8946-0B066D96E22B
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetOutputExtension method, ID3D11VideoContext.VideoProcessorSetOutputExtension, ID3D11VideoContext::VideoProcessorSetOutputExtension, VideoProcessorSetOutputExtension, VideoProcessorSetOutputExtension method [Media Foundation], VideoProcessorSetOutputExtension method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetOutputExtension, mf.id3d11videocontext_videoprocessorsetoutputextension
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ID3D11VideoContext.VideoProcessorSetOutputExtension
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoContext::VideoProcessorSetOutputExtension


## -description


Sets a driver-specific video processing state.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param pExtensionGuid [in]

A pointer to a GUID that identifies the operation. The meaning of this GUID is defined by the graphics driver.


### -param DataSize [in]

The size of the <i>pData</i> buffer, in bytes.


### -param pData [in]

A pointer to a buffer that contains private state data. The method passes this buffer directly to the driver without validation. It is the responsibility of the driver to validate the data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

