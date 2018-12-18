---
UID: NF:windows.media.streaming.IActiveBasicDeviceStatics.CreateBasicDeviceAsync
title: IActiveBasicDeviceStatics::streaming
author: windows-sdk-content
description: Asynchronously creates an active basic device.
old-location: mediastreaming\iactivebasicdevicestatics_createbasicdeviceasync.htm
tech.root: mediastreaming
ms.assetid: 52342B15-6250-4D46-9188-CC7AD98F09F7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateBasicDeviceAsync, CreateBasicDeviceAsync method [Media Streaming API], CreateBasicDeviceAsync method [Media Streaming API],IActiveBasicDeviceStatics interface, IActiveBasicDeviceStatics interface [Media Streaming API],CreateBasicDeviceAsync method, IActiveBasicDeviceStatics.CreateBasicDeviceAsync, IActiveBasicDeviceStatics.streaming, IActiveBasicDeviceStatics::CreateBasicDeviceAsync, IActiveBasicDeviceStatics::streaming, mediastreaming.iactivebasicdevicestatics_createbasicdeviceasync, windows/IActiveBasicDeviceStatics::CreateBasicDeviceAsync
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
 - IActiveBasicDeviceStatics.CreateBasicDeviceAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveBasicDeviceStatics::streaming


## -description


Asynchronously creates an active basic device.


## -parameters




### -param deviceIdentifier [in]

The identifier of the device. 


### -param type [in]

The type of the device.


### -param value [out, retval]

The asynchronous operation. Upon completion, <a href="https://msdn.microsoft.com/1E40AEED-8D57-4FBC-AF25-11B27399477C">IAsyncOperation.GetResults</a> returns a <a href="https://msdn.microsoft.com/B747505A-7F8F-44F4-A9B3-73A8FE424D5F">ActiveBasicDevice</a> object.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/B747505A-7F8F-44F4-A9B3-73A8FE424D5F">ActiveBasicDevice</a>



<a href="https://msdn.microsoft.com/89A080E7-593B-406F-9E9B-4EC5838A619E">BasicDevice</a>



<a href="https://msdn.microsoft.com/B4D8BAEF-AD30-4FEC-9527-583E88C8B4C7">IActiveBasicDeviceStatics</a>
 

 

