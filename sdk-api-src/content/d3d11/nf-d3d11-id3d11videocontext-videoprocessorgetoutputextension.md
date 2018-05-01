---
UID: NF:d3d11.ID3D11VideoContext.VideoProcessorGetOutputExtension
title: ID3D11VideoContext::VideoProcessorGetOutputExtension method
author: windows-driver-content
description: Gets private state data from the video processor.
old-location: mf\id3d11videocontext_videoprocessorgetoutputextension.htm
old-project: medfound
ms.assetid: 3B979D5D-CB3D-4B67-9BE3-277005076604
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: ID3D11VideoContext, ID3D11VideoContext interface [Media Foundation], VideoProcessorGetOutputExtension method, ID3D11VideoContext::VideoProcessorGetOutputExtension, VideoProcessorGetOutputExtension method [Media Foundation], VideoProcessorGetOutputExtension method [Media Foundation], ID3D11VideoContext interface, VideoProcessorGetOutputExtension,ID3D11VideoContext.VideoProcessorGetOutputExtension, d3d11/ID3D11VideoContext::VideoProcessorGetOutputExtension, mf.id3d11videocontext_videoprocessorgetoutputextension
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
-	ID3D11VideoContext.VideoProcessorGetOutputExtension
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D11VideoContext::VideoProcessorGetOutputExtension method


## -description


Gets private state data from the video processor.


## -parameters




### -param pVideoProcessor [in]

A pointer to the <a href="https://msdn.microsoft.com/AF6F6781-A7F9-4196-8E91-FDFDD1924E24">ID3D11VideoProcessor</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/5A5FB7F9-F299-4E67-AFAD-E7056CBAEE76">ID3D11VideoDevice::CreateVideoProcessor</a>.


### -param pExtensionGuid [in]

A pointer to a GUID that identifies the state. The meaning of this GUID is defined by the graphics driver.


### -param DataSize [in]

The size of the <i>pData</i> buffer, in bytes.


### -param pData [out]

A pointer to a buffer that receives the private state data. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

