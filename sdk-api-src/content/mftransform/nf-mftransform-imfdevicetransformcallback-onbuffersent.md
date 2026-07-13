---
UID: NF:mftransform.IMFDeviceTransformCallback.OnBufferSent
title: IMFDeviceTransformCallback::OnBufferSent (mftransform.h)
description: Called when system-allocated frame buffers are sent to the device driver.
helpviewer_keywords: ["IMFDeviceTransformCallback interface [Streaming Media Devices]","OnBufferSent method","IMFDeviceTransformCallback.OnBufferSent","IMFDeviceTransformCallback::OnBufferSent","OnBufferSent","OnBufferSent method [Streaming Media Devices]","OnBufferSent method [Streaming Media Devices]","IMFDeviceTransformCallback interface","mftransform/IMFDeviceTransformCallback::OnBufferSent","stream.imfdevicetransformcallback_onbuffersent"]
old-location: stream\imfdevicetransformcallback_onbuffersent.htm
tech.root: stream
ms.assetid: 8736BF02-636A-4894-AA74-92A805152D52
ms.date: 12/05/2018
ms.keywords: IMFDeviceTransformCallback interface [Streaming Media Devices],OnBufferSent method, IMFDeviceTransformCallback.OnBufferSent, IMFDeviceTransformCallback::OnBufferSent, OnBufferSent, OnBufferSent method [Streaming Media Devices], OnBufferSent method [Streaming Media Devices],IMFDeviceTransformCallback interface, mftransform/IMFDeviceTransformCallback::OnBufferSent, stream.imfdevicetransformcallback_onbuffersent
req.header: mftransform.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFDeviceTransformCallback::OnBufferSent
 - mftransform/IMFDeviceTransformCallback::OnBufferSent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mftransform.h
api_name:
 - IMFDeviceTransformCallback.OnBufferSent
---

# IMFDeviceTransformCallback::OnBufferSent


## -description



Called when system-allocated frame buffers are sent to the device driver.

## -parameters

### -param pCallbackAttributes

The attributes containing the callback data. The System-allocated frame buffer information is stored in the attribute with the MF_DMFT_FRAME_BUFFER_INFO key.

### -param pinId

The identifier of the device pin to which the frame buffers are sent.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The frame buffer header information provided by this callback is read-only. You should not try to allocate, deallocate, open, or close anything within the header.

## -see-also

<a href="/windows/desktop/api/mftransform/nn-mftransform-imfdevicetransformcallback">IMFDeviceTransformCallback</a>