---
UID: NF:portabledeviceapi.IPortableDeviceEventCallback.OnEvent
title: IPortableDeviceEventCallback::OnEvent
author: windows-sdk-content
description: The OnEvent method is called by the SDK to notify the application about asynchronous events.
old-location: wpdsdk\iportabledeviceeventcallback_onevent.htm
old-project: wpd_sdk
ms.assetid: 14659de0-5cea-458a-bf57-fe8b071c778a
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IPortableDeviceEventCallback interface [Windows Portable Devices SDK],OnEvent method, IPortableDeviceEventCallback.OnEvent, IPortableDeviceEventCallback::OnEvent, IPortableDeviceEventCallbackOnEvent, OnEvent, OnEvent method [Windows Portable Devices SDK], OnEvent method [Windows Portable Devices SDK],IPortableDeviceEventCallback interface, portabledeviceapi/IPortableDeviceEventCallback::OnEvent, wpdsdk.iportabledeviceeventcallback_onevent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceEventCallback.OnEvent
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceEventCallback::OnEvent


## -description



The <b>OnEvent</b> method is called by the SDK to notify the application about asynchronous events.




## -parameters




### -param pEventParameters [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that contains event details.


## -returns



Any values returned by the application are ignored by Windows Portable Devices.




## -remarks



The application must register to receive events by calling <a href="https://msdn.microsoft.com/bab28a19-7ba2-4edd-b5aa-c2017b4bf8ca">IPortableDevice::Advise</a>.


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/529a8b7a-08b4-47de-8ed3-28e8fff0ede2">Handling Events from the Device</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/529a8b7a-08b4-47de-8ed3-28e8fff0ede2">Handling Events from the Device</a>



<a href="https://msdn.microsoft.com/1fb2d5d8-82b8-4c51-a086-bdcad33da190">IPortableDeviceEventCallback Interface</a>
 

 

