---
UID: NF:upnp.IUPnPDescriptionDocument.DeviceByUDN
title: IUPnPDescriptionDocument::DeviceByUDN (upnp.h)
description: The DeviceByUDN method returns the device with the specified unique device name (UDN) contained within the loaded description document.
helpviewer_keywords: ["DeviceByUDN","DeviceByUDN method [UPnP APIs]","DeviceByUDN method [UPnP APIs]","IUPnPDescriptionDocument interface","IUPnPDescriptionDocument interface [UPnP APIs]","DeviceByUDN method","IUPnPDescriptionDocument.DeviceByUDN","IUPnPDescriptionDocument::DeviceByUDN","_upnp_iupnpdescriptiondocument_devicebyudn","upnp.iupnpdescriptiondocument_devicebyudn","upnp/IUPnPDescriptionDocument::DeviceByUDN"]
old-location: upnp\iupnpdescriptiondocument_devicebyudn.htm
tech.root: upnp
ms.assetid: 0f8ae379-3ec6-4fe2-ae7b-fe3750a5d4c3
ms.date: 12/05/2018
ms.keywords: DeviceByUDN, DeviceByUDN method [UPnP APIs], DeviceByUDN method [UPnP APIs],IUPnPDescriptionDocument interface, IUPnPDescriptionDocument interface [UPnP APIs],DeviceByUDN method, IUPnPDescriptionDocument.DeviceByUDN, IUPnPDescriptionDocument::DeviceByUDN, _upnp_iupnpdescriptiondocument_devicebyudn, upnp.iupnpdescriptiondocument_devicebyudn, upnp/IUPnPDescriptionDocument::DeviceByUDN
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
 - IUPnPDescriptionDocument::DeviceByUDN
 - upnp/IUPnPDescriptionDocument::DeviceByUDN
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
 - IUPnPDescriptionDocument.DeviceByUDN
---

# IUPnPDescriptionDocument::DeviceByUDN


## -description

The 
<b>DeviceByUDN</b> method returns the device with the specified unique device name (UDN) contained within the loaded description document.

## -parameters

### -param bstrUDN [in]

Specifies the UDN of the device.

### -param ppudDevice [out]

Receives a reference to an 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> object that describes the device. This reference must be released when it is no longer used.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

Use 
<b>DeviceByUDN</b> after loading the device description using 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-load">IUPnPDescriptionDocument::Load</a> or 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-loadasync">IUPnPDescriptionDocument::LoadAsync</a>. The 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-get_readystate">IUPnPDescriptionDocument::ReadyState</a> property returns READYSTATE_COMPLETED.

Do not use 
<b>DeviceByUDN</b> unless a device description is first loaded using either 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-load">IUPnPDescriptionDocument::Load</a> or 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-loadasync">IUPnPDescriptionDocument::LoadAsync</a>. The search operation only searches in the currently loaded device description.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocument">IUPnPDescriptionDocument</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>