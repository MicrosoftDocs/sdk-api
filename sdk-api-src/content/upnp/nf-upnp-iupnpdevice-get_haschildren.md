---
UID: NF:upnp.IUPnPDevice.get_HasChildren
title: IUPnPDevice::get_HasChildren
author: windows-sdk-content
description: The HasChildren property specifies whether the device has any child devices.
old-location: upnp\iupnpdevice_haschildren.htm
tech.root: UPnP
ms.assetid: 18a7c7e0-389d-4fc4-b98c-4eb1afea4a7e
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_HasChildren method, IUPnPDevice.get_HasChildren, IUPnPDevice::get_HasChildren, _upnp_iupnpdevice_haschildren, get_HasChildren, get_HasChildren method [UPnP APIs], get_HasChildren method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_haschildren, upnp/IUPnPDevice::get_HasChildren
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
 - IUPnPDevice.get_HasChildren
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- upnp.h
: 
- IUPnPDevice.get_HasChildren
: 
---

# IUPnPDevice::get_HasChildren


## -description


The 
<b>HasChildren</b> property specifies whether the device has any child devices.


## -parameters




### -param pvarb [out]

Receives a reference to a <b>VARIANT_BOOL</b> that contains the value VARIANT_TRUE if the device has one or more child devices; otherwise, it contains the value VARIANT_FALSE.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



Use this property to determine whether or not the application should access the <a href="https://msdn.microsoft.com/a8cdc66f-c5c0-4328-a8f2-f40d55a20a4f">IUPnPDevice::Children</a> property.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>



<a href="https://msdn.microsoft.com/a8cdc66f-c5c0-4328-a8f2-f40d55a20a4f">IUPnPDevice::Children</a>
 

 

