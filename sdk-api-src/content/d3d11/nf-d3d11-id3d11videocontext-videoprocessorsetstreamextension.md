---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorSetStreamExtension
title: ID3D11VideoContext::VideoProcessorSetStreamExtension
author: windows-driver-content
description: Sets a driver-specific state on a video processing stream.
old-location: mf\id3d11videocontext_videoprocessorsetstreamextension.htm
old-project: medfound
ms.assetid: E6E1CF26-6A9F-42E1-8DA7-2AC76CE05906
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],VideoProcessorSetStreamExtension method, ID3D11VideoContext.VideoProcessorSetStreamExtension, ID3D11VideoContext::VideoProcessorSetStreamExtension, VideoProcessorSetStreamExtension, VideoProcessorSetStreamExtension method [Media Foundation], VideoProcessorSetStreamExtension method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::VideoProcessorSetStreamExtension, mf.id3d11videocontext_videoprocessorsetstreamextension
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
req.typenames: D3D11_VPOV_DIMENSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	d3d11.h
api_name:
-	ID3D11VideoContext.VideoProcessorSetStreamExtension
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

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param StreamIndex [in]

The zero-based index of the input stream. To get the maximum number of streams, call <a href="https://msdn.microsoft.com/BE213FFE-FB1D-4BDC-A1AA-2EA487DF8D4A">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>MaxStreamStates</b> structure member.


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
 

 

