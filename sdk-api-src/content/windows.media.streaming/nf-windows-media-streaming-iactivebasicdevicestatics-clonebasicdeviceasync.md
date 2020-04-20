---
UID: NF:windows.media.streaming.IActiveBasicDeviceStatics.CloneBasicDeviceAsync
title: IActiveBasicDeviceStatics::streaming (windows.media.streaming.h)
description: Asynchronously creates a clone of a basic device.helpviewer_keywords: ["CloneBasicDeviceAsync","CloneBasicDeviceAsync method [Media Streaming API]","CloneBasicDeviceAsync method [Media Streaming API]","IActiveBasicDeviceStatics interface","IActiveBasicDeviceStatics interface [Media Streaming API]","CloneBasicDeviceAsync method","IActiveBasicDeviceStatics.CloneBasicDeviceAsync","IActiveBasicDeviceStatics.streaming","IActiveBasicDeviceStatics::CloneBasicDeviceAsync","IActiveBasicDeviceStatics::streaming","mediastreaming.iactivebasicdevicestatics_clonebasicdeviceasync","windows/IActiveBasicDeviceStatics::CloneBasicDeviceAsync"]
old-location: mediastreaming\iactivebasicdevicestatics_clonebasicdeviceasync.htm
tech.root: mediastreaming
ms.assetid: B79B569D-FADF-437E-A2F5-DB9C176F570C
ms.date: 12/05/2018
ms.keywords: CloneBasicDeviceAsync, CloneBasicDeviceAsync method [Media Streaming API], CloneBasicDeviceAsync method [Media Streaming API],IActiveBasicDeviceStatics interface, IActiveBasicDeviceStatics interface [Media Streaming API],CloneBasicDeviceAsync method, IActiveBasicDeviceStatics.CloneBasicDeviceAsync, IActiveBasicDeviceStatics.streaming, IActiveBasicDeviceStatics::CloneBasicDeviceAsync, IActiveBasicDeviceStatics::streaming, mediastreaming.iactivebasicdevicestatics_clonebasicdeviceasync, windows/IActiveBasicDeviceStatics::CloneBasicDeviceAsync
f1_keywords:
- windows.media.streaming/IActiveBasicDeviceStatics.CloneBasicDeviceAsync
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- PlayToDevice.dll
api_name:
- IActiveBasicDeviceStatics.CloneBasicDeviceAsync
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActiveBasicDeviceStatics::streaming


## -description


Asynchronously creates a clone of a basic device.


## -parameters




### -param basicDevice [in]

The basic device object to clone.


### -param value [out, retval]

The asynchronous operation. Upon completion, <a href="https://docs.microsoft.com/previous-versions/br205815(v=vs.85)">IAsyncOperation.GetResults</a> returns a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)">ActiveBasicDevice</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn385755(v=vs.85)">ActiveBasicDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh828813(v=vs.85)">BasicDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-iactivebasicdevicestatics">IActiveBasicDeviceStatics</a>
 

 

