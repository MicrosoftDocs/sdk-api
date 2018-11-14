---
UID: NF:windows.media.streaming.IActiveBasicDevice.GetEffectiveBandwidth
title: IActiveBasicDevice::streaming
author: windows-sdk-content
description: Gets the current effective bandwidth for the device.
old-location: mediastreaming\iactivebasicdevice_geteffectivebandwidth.htm
tech.root: mediastreaming
ms.assetid: 894EC907-E578-4F1E-A0AB-1FDE2FA67B6C
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetEffectiveBandwidth, GetEffectiveBandwidth method [Media Streaming API], GetEffectiveBandwidth method [Media Streaming API],IActiveBasicDevice interface, IActiveBasicDevice interface [Media Streaming API],GetEffectiveBandwidth method, IActiveBasicDevice.GetEffectiveBandwidth, IActiveBasicDevice.streaming, IActiveBasicDevice::GetEffectiveBandwidth, IActiveBasicDevice::streaming, mediastreaming.iactivebasicdevice_geteffectivebandwidth, windows/IActiveBasicDevice::GetEffectiveBandwidth
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
 - IActiveBasicDevice.GetEffectiveBandwidth
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
- IActiveBasicDevice.GetEffectiveBandwidth
: 
---

# IActiveBasicDevice::streaming


## -description


Gets the current effective bandwidth for the device.


## -parameters




### -param transmitSpeed [in, retval]

Specifies whether the transmit speed is retrieved or the receive speed is retrieved. 

<b>true</b> to retrieve the transmit speed. <b>false</b> to retrieve the receive speed.


### -param currentSpeed [out]

Receives the current effective bandwidth. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/97544BF4-188F-4CE3-9436-EB7F3E706E94">IActiveBasicDevice</a>



<a href="https://msdn.microsoft.com/E4F99A11-4ED5-44CB-BE16-CBB558412ED4">IBasicDevice</a>
 

 

