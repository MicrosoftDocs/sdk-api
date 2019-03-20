---
UID: NF:windows.media.streaming.IActiveBasicDevice.SetCachedBitrateMeasurement
title: IActiveBasicDevice::streaming (windows.media.streaming.h)
author: windows-sdk-content
description: Sets the cached bitrate.
old-location: mediastreaming\iactivebasicdevice_setcachedbitratemeasurement.htm
tech.root: mediastreaming
ms.assetid: B695D51C-205B-4D45-BEA7-0235FC770C77
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IActiveBasicDevice interface [Media Streaming API],SetCachedBitrateMeasurement method, IActiveBasicDevice.SetCachedBitrateMeasurement, IActiveBasicDevice.streaming, IActiveBasicDevice::SetCachedBitrateMeasurement, IActiveBasicDevice::streaming, SetCachedBitrateMeasurement, SetCachedBitrateMeasurement method [Media Streaming API], SetCachedBitrateMeasurement method [Media Streaming API],IActiveBasicDevice interface, mediastreaming.iactivebasicdevice_setcachedbitratemeasurement, windows/IActiveBasicDevice::SetCachedBitrateMeasurement
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
 - IActiveBasicDevice.SetCachedBitrateMeasurement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveBasicDevice::streaming


## -description


Sets the cached bitrate.


## -parameters




### -param physicalNetworkInterface [in]

Specifies the physical network interface.


### -param bitrate [in]

The value to set the bitrate to.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/97544BF4-188F-4CE3-9436-EB7F3E706E94">IActiveBasicDevice</a>



<a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a>
 

 

