---
UID: NF:mftransform.IMFDeviceTransformCallback.OnBufferSent
title: IMFDeviceTransformCallback::OnBufferSent
author: windows-sdk-content
description: Called when system-allocated frame buffers are sent to the device driver.
old-location: stream\imfdevicetransformcallback_onbuffersent.htm
old-project: stream
ms.assetid: 8736BF02-636A-4894-AA74-92A805152D52
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IMFDeviceTransformCallback interface [Streaming Media Devices],OnBufferSent method, IMFDeviceTransformCallback.OnBufferSent, IMFDeviceTransformCallback::OnBufferSent, OnBufferSent, OnBufferSent method [Streaming Media Devices], OnBufferSent method [Streaming Media Devices],IMFDeviceTransformCallback interface, mftransform/IMFDeviceTransformCallback::OnBufferSent, stream.imfdevicetransformcallback_onbuffersent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mftransform.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803
req.target-min-winversvr: Windows Server 2016
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mftransform.h
api_name:
 - IMFDeviceTransformCallback.OnBufferSent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFDeviceTransformCallback::OnBufferSent


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Called when system-allocated frame buffers are sent to the device driver. 


## -parameters




### -param pCallbackAttributes

The attributes containing the callback data. The System-allocated frame buffer information is stored in the attribute with the MF_DMFT_FRAME_BUFFER_INFO key. 


### -param pinId

The identifier of the device pin to which the frame buffers are sent.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The frame buffer header information provided by this callback is read-only. You should not try to allocate, deallocate, open, or close anything within the header.




## -see-also




<a href="https://msdn.microsoft.com/library/Mt846762(v=VS.85).aspx">IMFDeviceTransformCallback</a>
 

 

