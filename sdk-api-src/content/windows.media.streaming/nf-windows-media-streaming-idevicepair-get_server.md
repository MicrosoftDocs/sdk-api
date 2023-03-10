---
UID: NF:windows.media.streaming.IDevicePair.get_Server
title: IDevicePair::streaming (windows.media.streaming.h)
description: Gets the server for the active basic device pair.
helpviewer_keywords: ["IDevicePair interface [Media Streaming API]","get_Server method","IDevicePair.get_Server","IDevicePair.streaming","IDevicePair::get_Server","IDevicePair::streaming","get_Server","get_Server method [Media Streaming API]","get_Server method [Media Streaming API]","IDevicePair interface","mediastreaming.idevicepair_server","windows/IDevicePair::get_Server"]
old-location: mediastreaming\idevicepair_server.htm
tech.root: mediastreaming
ms.assetid: F362617D-E0F8-4F2C-8968-93AD25FE0990
ms.date: 12/05/2018
ms.keywords: IDevicePair interface [Media Streaming API],get_Server method, IDevicePair.get_Server, IDevicePair.streaming, IDevicePair::get_Server, IDevicePair::streaming, get_Server, get_Server method [Media Streaming API], get_Server method [Media Streaming API],IDevicePair interface, mediastreaming.idevicepair_server, windows/IDevicePair::get_Server
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
 - IDevicePair::get_Server
 - windows.media.streaming/IDevicePair::get_Server
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
 - IDevicePair.get_Server
---

# IDevicePair::streaming


## -description

Gets the server for the active basic device pair.

## -parameters

### -param value [out, retval]

Receives the server device.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)">ActiveBasicDevice</a>



<a href="/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevice">IActiveBasicDevice</a>



<a href="/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-idevicepair">IDevicePair</a>