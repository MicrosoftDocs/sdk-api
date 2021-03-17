---
UID: NF:upnp.IUPnPDeviceFinder.FindByType
title: IUPnPDeviceFinder::FindByType (upnp.h)
description: The FindByType method searches synchronously for devices by device type or service type.
helpviewer_keywords: ["FindByType","FindByType method [UPnP APIs]","FindByType method [UPnP APIs]","IUPnPDeviceFinder interface","IUPnPDeviceFinder interface [UPnP APIs]","FindByType method","IUPnPDeviceFinder.FindByType","IUPnPDeviceFinder::FindByType","_upnp_iupnpdevicefinder_findbytype","upnp.iupnpdevicefinder_findbytype","upnp/IUPnPDeviceFinder::FindByType"]
old-location: upnp\iupnpdevicefinder_findbytype.htm
tech.root: upnp
ms.assetid: 5fc28829-8802-457b-a1cf-c74834b6651c
ms.date: 12/05/2018
ms.keywords: FindByType, FindByType method [UPnP APIs], FindByType method [UPnP APIs],IUPnPDeviceFinder interface, IUPnPDeviceFinder interface [UPnP APIs],FindByType method, IUPnPDeviceFinder.FindByType, IUPnPDeviceFinder::FindByType, _upnp_iupnpdevicefinder_findbytype, upnp.iupnpdevicefinder_findbytype, upnp/IUPnPDeviceFinder::FindByType
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
 - IUPnPDeviceFinder::FindByType
 - upnp/IUPnPDeviceFinder::FindByType
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
 - IUPnPDeviceFinder.FindByType
---

# IUPnPDeviceFinder::FindByType


## -description

The 
<b>FindByType</b> method searches synchronously for devices by device type or service type.

## -parameters

### -param bstrTypeURI [in]

Specifies the type URI for the device or service type for which to search.

### -param dwFlags [in]

Must be zero. This parameter is reserved for future use.

### -param pDevices [out]

Receives a reference to a collection of 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevices">IUPnPDevices</a> devices that were found.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

This method does not return until the search is complete. The search can take at least nine seconds, and possibly more. This method must not be called from a thread that processes user interface messages.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-findbyudn">IUPnPDeviceFinder::FindByUDN</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevices">IUPnPDevices</a>