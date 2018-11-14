---
UID: NF:upnp.IUPnPDevice.get_Type
title: IUPnPDevice::get_Type
author: windows-sdk-content
description: The Type method specifies the device type uniform resource identifier (URI) for the device.
old-location: upnp\iupnpdevice_type.htm
tech.root: UPnP
ms.assetid: 3db09e94-4211-44ff-850e-2e34719909d6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_Type method, IUPnPDevice.get_Type, IUPnPDevice::get_Type, _upnp_iupnpdevice_type, get_Type, get_Type method [UPnP APIs], get_Type method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_type, upnp/IUPnPDevice::get_Type
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
 - IUPnPDevice.get_Type
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
- IUPnPDevice.get_Type
: 
---

# IUPnPDevice::get_Type


## -description


The 
<b>Type</b> method specifies the device type uniform resource identifier (URI) for the device.


## -parameters




### -param pbstr [out]

Receives a reference to a string that contains the device type's URI. Release this string with <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> when it is no longer required.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>
 

 

