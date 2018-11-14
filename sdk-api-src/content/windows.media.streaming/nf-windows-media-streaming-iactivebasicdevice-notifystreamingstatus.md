---
UID: NF:windows.media.streaming.IActiveBasicDevice.NotifyStreamingStatus
title: IActiveBasicDevice::streaming
author: windows-sdk-content
description: Called by the application to indicate that the device is being used for active streaming.
old-location: mediastreaming\iactivebasicdevice_notifystreamingstatus.htm
tech.root: mediastreaming
ms.assetid: D62E8571-1DE9-4BAB-A291-415FD6E9F9C8
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IActiveBasicDevice interface [Media Streaming API],NotifyStreamingStatus method, IActiveBasicDevice.NotifyStreamingStatus, IActiveBasicDevice.streaming, IActiveBasicDevice::NotifyStreamingStatus, IActiveBasicDevice::streaming, NotifyStreamingStatus, NotifyStreamingStatus method [Media Streaming API], NotifyStreamingStatus method [Media Streaming API],IActiveBasicDevice interface, mediastreaming.iactivebasicdevice_notifystreamingstatus, windows/IActiveBasicDevice::NotifyStreamingStatus
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
 - IActiveBasicDevice.NotifyStreamingStatus
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
- IActiveBasicDevice.NotifyStreamingStatus
: 
---

# IActiveBasicDevice::streaming


## -description


Called by the application to indicate  that  the device is being used for active streaming. 


## -parameters




### -param fIsStreaming

<b>true</b> indicates that streaming is on.  <b>false</b> indicates that streaming if off.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is  called by the application to indicate that the device is being used for active streaming. A value of <b>true</b> means that streaming is on. A value of <b>false</b> means that streaming is off.  

The on/off calls must be matching calls from the application.

In response to this notification, the <a href="https://msdn.microsoft.com/B747505A-7F8F-44F4-A9B3-73A8FE424D5F">ActiveBasicDevice</a> object can take actions to keep the connection to the device active.




## -see-also




<a href="https://msdn.microsoft.com/97544BF4-188F-4CE3-9436-EB7F3E706E94">IActiveBasicDevice</a>
 

 

