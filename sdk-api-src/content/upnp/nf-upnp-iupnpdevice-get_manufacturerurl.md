---
UID: NF:upnp.IUPnPDevice.get_ManufacturerURL
title: IUPnPDevice::get_ManufacturerURL (upnp.h)
description: The ManufacturerURL property specifies the URL for the manufacturer's Web site.
helpviewer_keywords: ["IUPnPDevice interface [UPnP APIs]","get_ManufacturerURL method","IUPnPDevice.get_ManufacturerURL","IUPnPDevice::get_ManufacturerURL","_upnp_iupnpdevice_manufacturerurl","get_ManufacturerURL","get_ManufacturerURL method [UPnP APIs]","get_ManufacturerURL method [UPnP APIs]","IUPnPDevice interface","upnp.iupnpdevice_manufacturerurl","upnp/IUPnPDevice::get_ManufacturerURL"]
old-location: upnp\iupnpdevice_manufacturerurl.htm
tech.root: upnp
ms.assetid: 7019716a-4a64-43cd-bb44-21bdb6b022c2
ms.date: 12/05/2018
ms.keywords: IUPnPDevice interface [UPnP APIs],get_ManufacturerURL method, IUPnPDevice.get_ManufacturerURL, IUPnPDevice::get_ManufacturerURL, _upnp_iupnpdevice_manufacturerurl, get_ManufacturerURL, get_ManufacturerURL method [UPnP APIs], get_ManufacturerURL method [UPnP APIs],IUPnPDevice interface, upnp.iupnpdevice_manufacturerurl, upnp/IUPnPDevice::get_ManufacturerURL
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
 - IUPnPDevice::get_ManufacturerURL
 - upnp/IUPnPDevice::get_ManufacturerURL
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
 - IUPnPDevice.get_ManufacturerURL
---

# IUPnPDevice::get_ManufacturerURL


## -description

The 
<b>ManufacturerURL</b> property specifies the URL for the manufacturer's Web site.

## -parameters

### -param pbstr [out]

Receives a reference to a string that contains the URL. Release this string with <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when it is no longer required. If the device does not specify this URL, this parameter is set to <b>NULL</b>.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. If the device does not specify this URL, the return value is S_FALSE and <i>pbstr</i> is <b>NULL</b>. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

This property is optional and <i>pbstr</i> can return <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevice-get_manufacturername">IUPnPDevice::ManufacturerName</a>