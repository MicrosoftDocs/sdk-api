---
UID: NS:dhcpcsdk._DHCPAPI_PARAMS
title: DHCPAPI_PARAMS (dhcpcsdk.h)
description: The DHCPAPI_PARAMS structure is used to request DHCP parameters.
helpviewer_keywords: ["*LPDHCPAPI_PARAMS","*LPDHCPAPI_PARAMS structure [DHCP]","*LPDHCPCAPI_PARAMS","*LPDHCPCAPI_PARAMS structure [DHCP]","*PDHCPAPI_PARAMS","*PDHCPAPI_PARAMS structure [DHCP]","*PDHCPCAPI_PARAMS","*PDHCPCAPI_PARAMS structure [DHCP]","DHCPAPI_PARAMS","DHCPAPI_PARAMS structure [DHCP]","DHCPCAPI_PARAMS","DHCPCAPI_PARAMS structure [DHCP]","dhcp.dhcpapi_params","dhcpcsdk/*LPDHCPAPI_PARAMS","dhcpcsdk/*LPDHCPCAPI_PARAMS","dhcpcsdk/*PDHCPAPI_PARAMS","dhcpcsdk/*PDHCPCAPI_PARAMS","dhcpcsdk/DHCPAPI_PARAMS","dhcpcsdk/DHCPCAPI_PARAMS"]
old-location: dhcp\dhcpapi_params.htm
tech.root: DHCP
ms.assetid: be8329a3-c3ad-4f5b-92ae-cf18fa847d53
ms.date: 12/05/2018
ms.keywords: '*LPDHCPAPI_PARAMS, *LPDHCPAPI_PARAMS structure [DHCP], *LPDHCPCAPI_PARAMS, *LPDHCPCAPI_PARAMS structure [DHCP], *PDHCPAPI_PARAMS, *PDHCPAPI_PARAMS structure [DHCP], *PDHCPCAPI_PARAMS, *PDHCPCAPI_PARAMS structure [DHCP], DHCPAPI_PARAMS, DHCPAPI_PARAMS structure [DHCP], DHCPCAPI_PARAMS, DHCPCAPI_PARAMS structure [DHCP], dhcp.dhcpapi_params, dhcpcsdk/*LPDHCPAPI_PARAMS, dhcpcsdk/*LPDHCPCAPI_PARAMS, dhcpcsdk/*PDHCPAPI_PARAMS, dhcpcsdk/*PDHCPCAPI_PARAMS, dhcpcsdk/DHCPAPI_PARAMS, dhcpcsdk/DHCPCAPI_PARAMS'
req.header: dhcpcsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: DHCPAPI_PARAMS, *PDHCPAPI_PARAMS, *LPDHCPAPI_PARAMS, DHCPCAPI_PARAMS, *PDHCPCAPI_PARAMS, *LPDHCPCAPI_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPAPI_PARAMS
 - dhcpcsdk/_DHCPAPI_PARAMS
 - PDHCPAPI_PARAMS
 - dhcpcsdk/PDHCPAPI_PARAMS
 - DHCPAPI_PARAMS
 - dhcpcsdk/DHCPAPI_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpcsdk.h
api_name:
 - DHCPAPI_PARAMS
---

# DHCPAPI_PARAMS structure


## -description

The <b>DHCPAPI_PARAMS</b> structure is used to request DHCP parameters.

## -struct-fields

### -field Flags

Reserved. Must be set to zero.

### -field OptionId

Identifier for the DHCP parameter being requested.

### -field IsVendor

Specifies whether the DHCP parameter is vendor-specific. Set to <b>TRUE</b> if the parameter is vendor-specific.

### -field Data.size_is

### -field Data.size_is.nBytesData

### -field Data

Pointer to the parameter data.

### -field nBytesData

Size of the data pointed to by <b>Data</b>, in bytes.

## -see-also

<a href="/windows/win32/api/dhcpcsdk/ns-dhcpcsdk-dhcpcapi_params_array">DHCPAPI_PARAMS_ARRAY</a>

