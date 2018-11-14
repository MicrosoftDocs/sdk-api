---
UID: NF:windows.media.streaming.IActiveBasicDeviceStatics.CloneBasicDeviceAsync
title: IActiveBasicDeviceStatics::streaming
author: windows-sdk-content
description: Asynchronously creates a clone of a basic device.
old-location: mediastreaming\iactivebasicdevicestatics_clonebasicdeviceasync.htm
tech.root: mediastreaming
ms.assetid: B79B569D-FADF-437E-A2F5-DB9C176F570C
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CloneBasicDeviceAsync, CloneBasicDeviceAsync method [Media Streaming API], CloneBasicDeviceAsync method [Media Streaming API],IActiveBasicDeviceStatics interface, IActiveBasicDeviceStatics interface [Media Streaming API],CloneBasicDeviceAsync method, IActiveBasicDeviceStatics.CloneBasicDeviceAsync, IActiveBasicDeviceStatics.streaming, IActiveBasicDeviceStatics::CloneBasicDeviceAsync, IActiveBasicDeviceStatics::streaming, mediastreaming.iactivebasicdevicestatics_clonebasicdeviceasync, windows/IActiveBasicDeviceStatics::CloneBasicDeviceAsync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- windows.media.streaming.h
: 
- IActiveBasicDeviceStatics.CloneBasicDeviceAsync
: 
---

# IActiveBasicDeviceStatics::streaming


## -description


Asynchronously creates a clone of a basic device.


## -parameters




### -param basicDevice [in]

The basic device object to clone.


### -param value [out, retval]

The asynchronous operation. Upon completion, <a href="https://msdn.microsoft.com/1E40AEED-8D57-4FBC-AF25-11B27399477C">IAsyncOperation.GetResults</a> returns a <a href="https://msdn.microsoft.com/B747505A-7F8F-44F4-A9B3-73A8FE424D5F">ActiveBasicDevice</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B747505A-7F8F-44F4-A9B3-73A8FE424D5F">ActiveBasicDevice</a>



<a href="https://msdn.microsoft.com/89A080E7-593B-406F-9E9B-4EC5838A619E">BasicDevice</a>



<a href="https://msdn.microsoft.com/B4D8BAEF-AD30-4FEC-9527-583E88C8B4C7">IActiveBasicDeviceStatics</a>
 

 

