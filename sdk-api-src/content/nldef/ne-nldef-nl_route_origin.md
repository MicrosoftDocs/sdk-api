---
UID: NE:nldef._NL_ROUTE_ORIGIN
title: NL_ROUTE_ORIGIN (nldef.h)
description: The NL_ROUTE_ORIGIN enumeration type defines the origin of the IP route.
helpviewer_keywords: ["*PNL_ROUTE_ORIGIN","NL_ROUTE_ORIGIN","NL_ROUTE_ORIGIN enumeration [Network Drivers Starting with Windows Vista]","Nlro6to4","NlroDHCP","NlroManual","NlroRouterAdvertisement","NlroWellKnown","PNL_ROUTE_ORIGIN","PNL_ROUTE_ORIGIN enumeration pointer [Network Drivers Starting with Windows Vista]","iphelper_f6fb2f16-6da7-4f32-895e-8dbb6929f81f.xml","netvista.nl_route_origin","nldef/NL_ROUTE_ORIGIN","nldef/Nlro6to4","nldef/NlroDHCP","nldef/NlroManual","nldef/NlroRouterAdvertisement","nldef/NlroWellKnown","nldef/PNL_ROUTE_ORIGIN"]
old-location: netvista\nl_route_origin.htm
tech.root: NetVista
ms.assetid: 15f45fe9-5a51-4b4b-ba34-cec2488cd1e0
ms.date: 12/05/2018
ms.keywords: '*PNL_ROUTE_ORIGIN, NL_ROUTE_ORIGIN, NL_ROUTE_ORIGIN enumeration [Network Drivers Starting with Windows Vista], Nlro6to4, NlroDHCP, NlroManual, NlroRouterAdvertisement, NlroWellKnown, PNL_ROUTE_ORIGIN, PNL_ROUTE_ORIGIN enumeration pointer [Network Drivers Starting with Windows Vista], iphelper_f6fb2f16-6da7-4f32-895e-8dbb6929f81f.xml, netvista.nl_route_origin, nldef/NL_ROUTE_ORIGIN, nldef/Nlro6to4, nldef/NlroDHCP, nldef/NlroManual, nldef/NlroRouterAdvertisement, nldef/NlroWellKnown, nldef/PNL_ROUTE_ORIGIN'
req.header: nldef.h
req.include-header: Netioapi.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating   systems.
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NL_ROUTE_ORIGIN, *PNL_ROUTE_ORIGIN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NL_ROUTE_ORIGIN
 - nldef/_NL_ROUTE_ORIGIN
 - PNL_ROUTE_ORIGIN
 - nldef/PNL_ROUTE_ORIGIN
 - NL_ROUTE_ORIGIN
 - nldef/NL_ROUTE_ORIGIN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - nldef.h
api_name:
 - NL_ROUTE_ORIGIN
---

# NL_ROUTE_ORIGIN enumeration


## -description

The NL_ROUTE_ORIGIN enumeration type defines the origin of the IP route.

## -enum-fields

### -field NlroManual

The route is a result of manual configuration.

### -field NlroWellKnown

The route is a well-known route.

### -field NlroDHCP

The route is a result of DHCP configuration.

### -field NlroRouterAdvertisement

The route is a result of router advertisement.

### -field Nlro6to4

The route is a result of 6to4 tunneling.

