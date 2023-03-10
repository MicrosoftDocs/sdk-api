---
UID: NF:upnp.IUPnPDevices.get__NewEnum
title: IUPnPDevices::get__NewEnum (upnp.h)
description: The _NewEnum property specifies either the IEnumVARIANT or IEnumUnknown enumerator interface for the collection. (IUPnPDevices.get__NewEnum)
helpviewer_keywords: ["IUPnPDevices interface [UPnP APIs]","get__NewEnum method","IUPnPDevices.get__NewEnum","IUPnPDevices::get__NewEnum","_upnp_iupnpdevices__newenum","get__NewEnum","get__NewEnum method [UPnP APIs]","get__NewEnum method [UPnP APIs]","IUPnPDevices interface","upnp.iupnpdevices__newenum","upnp/IUPnPDevices::get__NewEnum"]
old-location: upnp\iupnpdevices__newenum.htm
tech.root: upnp
ms.assetid: b4f2678d-8b3a-4208-b108-5474f3e54cb4
ms.date: 12/05/2018
ms.keywords: IUPnPDevices interface [UPnP APIs],get__NewEnum method, IUPnPDevices.get__NewEnum, IUPnPDevices::get__NewEnum, _upnp_iupnpdevices__newenum, get__NewEnum, get__NewEnum method [UPnP APIs], get__NewEnum method [UPnP APIs],IUPnPDevices interface, upnp.iupnpdevices__newenum, upnp/IUPnPDevices::get__NewEnum
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
 - IUPnPDevices::get__NewEnum
 - upnp/IUPnPDevices::get__NewEnum
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
 - IUPnPDevices.get__NewEnum
---

# IUPnPDevices::get__NewEnum


## -description

The 
<b>_NewEnum</b> property specifies either the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> or <a href="/windows/desktop/api/objidl/nn-objidl-ienumunknown">IEnumUnknown</a> enumerator interface for the collection.

## -parameters

### -param ppunk [out]

Receives a reference to the enumerator interface.

## -returns

For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

This property is not visible in Visual Basic; use the <b>for...each...next</b> programming construct instead.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevices">IUPnPDevices</a>
