---
UID: NF:upnp.IUPnPDeviceFinder.FindByUDN
title: IUPnPDeviceFinder::FindByUDN (upnp.h)
description: The FindByUDN method searches synchronously for a device by its unique device name (UDN).
helpviewer_keywords: ["FindByUDN","FindByUDN method [UPnP APIs]","FindByUDN method [UPnP APIs]","IUPnPDeviceFinder interface","IUPnPDeviceFinder interface [UPnP APIs]","FindByUDN method","IUPnPDeviceFinder.FindByUDN","IUPnPDeviceFinder::FindByUDN","_upnp_iupnpdevicefinder_findbyudn","upnp.iupnpdevicefinder_findbyudn","upnp/IUPnPDeviceFinder::FindByUDN"]
old-location: upnp\iupnpdevicefinder_findbyudn.htm
tech.root: upnp
ms.assetid: 88d4e004-7df8-45f4-b6ec-9dcf3f0ccfeb
ms.date: 12/05/2018
ms.keywords: FindByUDN, FindByUDN method [UPnP APIs], FindByUDN method [UPnP APIs],IUPnPDeviceFinder interface, IUPnPDeviceFinder interface [UPnP APIs],FindByUDN method, IUPnPDeviceFinder.FindByUDN, IUPnPDeviceFinder::FindByUDN, _upnp_iupnpdevicefinder_findbyudn, upnp.iupnpdevicefinder_findbyudn, upnp/IUPnPDeviceFinder::FindByUDN
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPDeviceFinder::FindByUDN
 - upnp/IUPnPDeviceFinder::FindByUDN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDeviceFinder.FindByUDN
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
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> object that contains the requested device. Receives <b>NULL</b> if the specified device is not found.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns S_FALSE.

## -remarks

This method returns as soon as a device that matches the specified UDN is found. If no device is found, the method takes at least nine seconds to return, and possibly longer.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-findbytype">IUPnPDeviceFinder::FindByType</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevices">IUPnPDevices</a>