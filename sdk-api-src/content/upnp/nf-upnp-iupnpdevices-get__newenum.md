---
UID: NF:upnp.IUPnPDevices.get__NewEnum
title: IUPnPDevices::get__NewEnum
author: windows-sdk-content
description: The _NewEnum property specifies either the IEnumVARIANT or IEnumUnknown enumerator interface for the collection.
old-location: upnp\iupnpdevices__newenum.htm
tech.root: upnp
ms.assetid: b4f2678d-8b3a-4208-b108-5474f3e54cb4
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IUPnPDevices interface [UPnP APIs],get__NewEnum method, IUPnPDevices.get__NewEnum, IUPnPDevices::get__NewEnum, _upnp_iupnpdevices__newenum, get__NewEnum, get__NewEnum method [UPnP APIs], get__NewEnum method [UPnP APIs],IUPnPDevices interface, upnp.iupnpdevices__newenum, upnp/IUPnPDevices::get__NewEnum
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
 - IUPnPDevices.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDevices::get__NewEnum


## -description


The 
<b>_NewEnum</b> property specifies either the <a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> or <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms683764">IEnumUnknown</a> enumerator interface for the collection.


## -parameters




### -param ppunk [out]

Receives a reference to the enumerator interface.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



This property is not visible in Visual Basic; use the <b>for...each...next</b> programming construct instead.




## -see-also




<a href="https://msdn.microsoft.com/237715dc-2b5a-45b4-b006-d31c0b4e89e3">IUPnPDevices</a>
 

 

