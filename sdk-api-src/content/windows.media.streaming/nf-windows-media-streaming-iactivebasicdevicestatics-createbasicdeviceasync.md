---
UID: NF:windows.media.streaming.IActiveBasicDeviceStatics.CreateBasicDeviceAsync
title: IActiveBasicDeviceStatics::streaming (windows.media.streaming.h)
description: Asynchronously creates an active basic device.
helpviewer_keywords: ["CreateBasicDeviceAsync","CreateBasicDeviceAsync method [Media Streaming API]","CreateBasicDeviceAsync method [Media Streaming API]","IActiveBasicDeviceStatics interface","IActiveBasicDeviceStatics interface [Media Streaming API]","CreateBasicDeviceAsync method","IActiveBasicDeviceStatics.CreateBasicDeviceAsync","IActiveBasicDeviceStatics.streaming","IActiveBasicDeviceStatics::CreateBasicDeviceAsync","IActiveBasicDeviceStatics::streaming","mediastreaming.iactivebasicdevicestatics_createbasicdeviceasync","windows/IActiveBasicDeviceStatics::CreateBasicDeviceAsync"]
old-location: mediastreaming\iactivebasicdevicestatics_createbasicdeviceasync.htm
tech.root: mediastreaming
ms.assetid: 52342B15-6250-4D46-9188-CC7AD98F09F7
ms.date: 4/26/2023
ms.keywords: CreateBasicDeviceAsync, CreateBasicDeviceAsync method [Media Streaming API], CreateBasicDeviceAsync method [Media Streaming API],IActiveBasicDeviceStatics interface, IActiveBasicDeviceStatics interface [Media Streaming API],CreateBasicDeviceAsync method, IActiveBasicDeviceStatics.CreateBasicDeviceAsync, IActiveBasicDeviceStatics.streaming, IActiveBasicDeviceStatics::CreateBasicDeviceAsync, IActiveBasicDeviceStatics::streaming, mediastreaming.iactivebasicdevicestatics_createbasicdeviceasync, windows/IActiveBasicDeviceStatics::CreateBasicDeviceAsync
req.header: windows.media.streaming.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.Media.Streaming.Devices.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: PlayToDevice.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActiveBasicDeviceStatics::CreateBasicDeviceAsync
 - windows.media.streaming/IActiveBasicDeviceStatics::CreateBasicDeviceAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PlayToDevice.dll
api_name:
 - IActiveBasicDeviceStatics.CreateBasicDeviceAsync
---

# IActiveBasicDeviceStatics::streaming


## -description

\[The feature associated with this page, [Windows Media Streaming API](/windows/win32/mediastreaming/media-streaming-api-portal), is a legacy feature. It has been superseded by [Media Casting](/windows/uwp/audio-video-camera/media-casting). **Media Casting** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Media Casting** instead of **Windows Media Streaming API**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Asynchronously creates an active basic device.

## -parameters

### -param deviceIdentifier [in]

The identifier of the device.

### -param type [in]

The type of the device.

### -param value [out, retval]

The asynchronous operation. Upon completion, <a href="/previous-versions/br205815(v=vs.85)">IAsyncOperation.GetResults</a> returns a <a href="/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)">ActiveBasicDevice</a> object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)">ActiveBasicDevice</a>



<a href="/previous-versions/windows/desktop/legacy/hh828813(v=vs.85)">BasicDevice</a>



<a href="/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics">IActiveBasicDeviceStatics</a>