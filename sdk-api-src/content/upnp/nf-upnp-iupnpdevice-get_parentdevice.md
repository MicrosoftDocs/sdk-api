---
UID: NF:upnp.IUPnPDevice.get_ParentDevice
title: IUPnPDevice::get_ParentDevice
author: windows-sdk-content
description: The ParentDevice property specifies the parent of the device.
old-location: upnp\iupnpdevice_parentdevice.htm
old-project: UPnP
ms.assetid: 662a0bda-32f5-4756-8851-e7b2d0b9cc44
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_ParentDevice method, IUPnPDevice.get_ParentDevice, IUPnPDevice::get_ParentDevice, _upnp_iupnpdevice_parentdevice, get_ParentDevice, get_ParentDevice method [UPnP APIs], get_ParentDevice method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_parentdevice, upnp/IUPnPDevice::get_ParentDevice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnp.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDevice.get_ParentDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnp.dll
req.irql: 
req.product: Windows UI
---

# IUPnPDevice::get_ParentDevice


## -description


The 
<b>ParentDevice</b> property specifies the parent of the device.


## -parameters




### -param ppudDeviceParent [out]

Receives a reference to an 
<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a> object that describes the parent device. This reference must be released when it is no longer required. If the device has no parent, it is a topmost device, and the parameter receives <b>NULL</b>.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. If the device is a topmost device, the return value is S_FALSE. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



To determine if the device has no parent, use <a href="https://msdn.microsoft.com/0416c4f0-1289-4e91-be34-23f8b80df5c3">IUPnPDevice::IsRootDevice</a>.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>



<a href="https://msdn.microsoft.com/a8cdc66f-c5c0-4328-a8f2-f40d55a20a4f">IUPnPDevice::Children</a>
 

 

