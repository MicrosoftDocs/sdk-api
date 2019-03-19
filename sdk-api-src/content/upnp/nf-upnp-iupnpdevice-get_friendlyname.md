---
UID: NF:upnp.IUPnPDevice.get_FriendlyName
title: IUPnPDevice::get_FriendlyName (upnp.h)
author: windows-sdk-content
description: The FriendlyName property specifies the device display name for the device.
old-location: upnp\iupnpdevice_friendlyname.htm
tech.root: upnp
ms.assetid: dd24384f-2657-4cb0-812e-1b51d53b73de
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_FriendlyName method, IUPnPDevice.get_FriendlyName, IUPnPDevice::get_FriendlyName, _upnp_iupnpdevice_friendlyname, get_FriendlyName, get_FriendlyName method [UPnP APIs], get_FriendlyName method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_friendlyname, upnp/IUPnPDevice::get_FriendlyName
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
 - IUPnPDevice.get_FriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDevice::get_FriendlyName


## -description


The 
<b>FriendlyName</b> property specifies the device display name for the device.


## -parameters




### -param pbstr [out]

Receives a reference to a string that contains the device display name. Release this string with <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a> when it is no longer required.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



It is possible for multiple devices to have the same display name. To determine if two device objects describe the same device, use the unique device name. For more information, see 
<a href="https://msdn.microsoft.com/ca644bd3-6580-44da-87f5-11d543814043">UniqueDeviceName</a>.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>



<a href="https://msdn.microsoft.com/ca644bd3-6580-44da-87f5-11d543814043">UniqueDeviceName</a>
 

 

