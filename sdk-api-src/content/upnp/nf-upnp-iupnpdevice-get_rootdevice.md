---
UID: NF:upnp.IUPnPDevice.get_RootDevice
title: IUPnPDevice::get_RootDevice
author: windows-sdk-content
description: The RootDevice property specifies the topmost device in the device tree. The root device represents a physical object.
old-location: upnp\iupnpdevice_rootdevice.htm
tech.root: upnp
ms.assetid: 6c6d1782-693a-4b23-b9e0-7e379ba7f96c
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_RootDevice method, IUPnPDevice.get_RootDevice, IUPnPDevice::get_RootDevice, _upnp_iupnpdevice_rootdevice, get_RootDevice, get_RootDevice method [UPnP APIs], get_RootDevice method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_rootdevice, upnp/IUPnPDevice::get_RootDevice
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUPnPDevice.get_RootDevice
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDevice::get_RootDevice


## -description


The 
<b>RootDevice</b> property specifies the topmost device in the device tree. The root device represents a physical object.


## -parameters




### -param ppudRootDevice [out]

Receives a reference to an 
<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a> object that describes the root device. This reference must be released when it is no longer required.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>



<a href="https://msdn.microsoft.com/0416c4f0-1289-4e91-be34-23f8b80df5c3">IUPnPDevice::IsRootDevice</a>
 

 

