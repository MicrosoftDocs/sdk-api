---
UID: NF:upnp.IUPnPDeviceFinder.FindByUDN
title: IUPnPDeviceFinder::FindByUDN
author: windows-sdk-content
description: The FindByUDN method searches synchronously for a device by its unique device name (UDN).
old-location: upnp\iupnpdevicefinder_findbyudn.htm
tech.root: UPnP
ms.assetid: 88d4e004-7df8-45f4-b6ec-9dcf3f0ccfeb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: FindByUDN, FindByUDN method [UPnP APIs], FindByUDN method [UPnP APIs],IUPnPDeviceFinder interface, IUPnPDeviceFinder interface [UPnP APIs],FindByUDN method, IUPnPDeviceFinder.FindByUDN, IUPnPDeviceFinder::FindByUDN, _upnp_iupnpdevicefinder_findbyudn, upnp.iupnpdevicefinder_findbyudn, upnp/IUPnPDeviceFinder::FindByUDN
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
 - IUPnPDeviceFinder.FindByUDN
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUPnPDeviceFinder::FindByUDN


## -description


The 
<b>FindByUDN</b> method searches synchronously for a device by its unique device name (UDN).


## -parameters




### -param bstrUDN [in]

Specifies the UDN for which to search. This value is case sensitive, and should be provided as  lower-case (e.g. uuid:e8f85dfd-ff...).


### -param pDevice [out]

Receives a reference to an 
<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a> object that contains the requested device. Receives <b>NULL</b> if the specified device is not found.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns S_FALSE.




## -remarks



This method returns as soon as a device that matches the specified UDN is found. If no device is found, the method takes at least nine seconds to return, and possibly longer.




## -see-also




<a href="https://msdn.microsoft.com/a4697038-8abc-42f2-9381-702fc82af90b">IUPnPDeviceFinder</a>



<a href="https://msdn.microsoft.com/5fc28829-8802-457b-a1cf-c74834b6651c">IUPnPDeviceFinder::FindByType</a>



<a href="https://msdn.microsoft.com/237715dc-2b5a-45b4-b006-d31c0b4e89e3">IUPnPDevices</a>
 

 

