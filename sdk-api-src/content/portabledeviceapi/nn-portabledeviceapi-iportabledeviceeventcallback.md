---
UID: NN:portabledeviceapi.IPortableDeviceEventCallback
title: IPortableDeviceEventCallback
author: windows-sdk-content
description: The IPortableDeviceEventCallback interface implemented by the application to receive asynchronous callbacks if an application has registered to receive them by calling IPortableDevice::Advise.
old-location: wpdsdk\iportabledeviceeventcallback.htm
tech.root: wpd_sdk
ms.assetid: 1fb2d5d8-82b8-4c51-a086-bdcad33da190
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IPortableDeviceEventCallback, IPortableDeviceEventCallback interface [Windows Portable Devices SDK], IPortableDeviceEventCallback interface [Windows Portable Devices SDK],described, IPortableDeviceEventCallbackInterface, portabledeviceapi/IPortableDeviceEventCallback, wpdsdk.iportabledeviceeventcallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceEventCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceEventCallback interface


## -description



The <b>IPortableDeviceEventCallback</b> interface implemented by the application to receive asynchronous callbacks if an application has registered to receive them by calling <a href="https://msdn.microsoft.com/bab28a19-7ba2-4edd-b5aa-c2017b4bf8ca">IPortableDevice::Advise</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceEventCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceEventCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceEventCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14659de0-5cea-458a-bf57-fe8b071c778a">OnEvent</a>
</td>
<td align="left" width="63%">
Called by the SDK to notify the application about asynchronous events.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fbe53f17-940a-485e-82b2-c11ae39b3300">Client Interfaces</a>
 

 

