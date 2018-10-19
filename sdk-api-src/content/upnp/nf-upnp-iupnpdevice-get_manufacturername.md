---
UID: NF:upnp.IUPnPDevice.get_ManufacturerName
title: IUPnPDevice::get_ManufacturerName
author: windows-sdk-content
description: The ManufacturerName property specifies a human-readable form of the manufacturer name of the device.
old-location: upnp\iupnpdevice_manufacturername.htm
tech.root: UPnP
ms.assetid: b62ba17d-4d0f-4609-ae34-0d8bd350f761
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_ManufacturerName method, IUPnPDevice.get_ManufacturerName, IUPnPDevice::get_ManufacturerName, _upnp_iupnpdevice_manufacturername, get_ManufacturerName, get_ManufacturerName method [UPnP APIs], get_ManufacturerName method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_manufacturername, upnp/IUPnPDevice::get_ManufacturerName
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
 - IUPnPDevice.get_ManufacturerName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDevice::get_ManufacturerName


## -description


The 
<b>ManufacturerName</b> property specifies a human-readable form of the manufacturer name of the device.


## -parameters




### -param pbstr [out]

Receives a reference to a string that contains the manufacturer's name. Release this string with <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when it is no longer required.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>



<a href="https://msdn.microsoft.com/7019716a-4a64-43cd-bb44-21bdb6b022c2">IUPnPDevice::ManufacturerURL</a>
 

 

