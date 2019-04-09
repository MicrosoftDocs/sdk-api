---
UID: NF:upnp.IUPnPDevice.get_IsRootDevice
title: IUPnPDevice::get_IsRootDevice (upnp.h)
author: windows-sdk-content
description: The IsRootDevice property specifies whether the device is the topmost device in the device tree.
old-location: upnp\iupnpdevice_isrootdevice.htm
tech.root: upnp
ms.assetid: 0416c4f0-1289-4e91-be34-23f8b80df5c3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_IsRootDevice method, IUPnPDevice.get_IsRootDevice, IUPnPDevice::get_IsRootDevice, _upnp_iupnpdevice_isrootdevice, get_IsRootDevice, get_IsRootDevice method [UPnP APIs], get_IsRootDevice method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_isrootdevice, upnp/IUPnPDevice::get_IsRootDevice
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDevice.get_IsRootDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDevice::get_IsRootDevice


## -description


The 
<b>IsRootDevice</b> property specifies whether the device is the topmost device in the device tree.


## -parameters




### -param pvarb [out]

Receives a reference to a <b>VARIANT_BOOL</b> that contains the value VARIANT_TRUE if the device is the topmost device in the device tree; otherwise, it contains the value VARIANT_FALSE.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>



<a href="https://msdn.microsoft.com/a8cdc66f-c5c0-4328-a8f2-f40d55a20a4f">IUPnPDevice::Children</a>



<a href="https://msdn.microsoft.com/6c6d1782-693a-4b23-b9e0-7e379ba7f96c">IUPnPDevice::RootDevice</a>
 

 

