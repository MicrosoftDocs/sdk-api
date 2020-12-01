---
UID: NS:dhcpv6csdk._DHCPV6CAPI_PARAMS_ARRAY
title: DHCPV6CAPI_PARAMS_ARRAY (dhcpv6csdk.h)
description: Contains an array of requested parameters.
helpviewer_keywords: ["*LPDHCPV6CAPI_PARAMS_ARRAY","*PDHCPV6CAPI_PARAMS_ARRAY","DHCPV6CAPI_PARAMS_ARRAY","DHCPV6CAPI_PARAMS_ARRAY structure [DHCP]","LPDHCPV6CAPI_PARAMS_ARRAY","LPDHCPV6CAPI_PARAMS_ARRAY structure pointer [DHCP]","PDHCPV6CAPI_PARAMS_ARRAY","PDHCPV6CAPI_PARAMS_ARRAY structure pointer [DHCP]","dhcp.dhcpv6capi_params_array","dhcpv6csdk/DHCPV6CAPI_PARAMS_ARRAY","dhcpv6csdk/LPDHCPV6CAPI_PARAMS_ARRAY","dhcpv6csdk/PDHCPV6CAPI_PARAMS_ARRAY"]
old-location: dhcp\dhcpv6capi_params_array.htm
tech.root: DHCP
ms.assetid: 2392586f-94a0-4667-b59a-88c0e1d88713
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV6CAPI_PARAMS_ARRAY, *PDHCPV6CAPI_PARAMS_ARRAY, DHCPV6CAPI_PARAMS_ARRAY, DHCPV6CAPI_PARAMS_ARRAY structure [DHCP], LPDHCPV6CAPI_PARAMS_ARRAY, LPDHCPV6CAPI_PARAMS_ARRAY structure pointer [DHCP], PDHCPV6CAPI_PARAMS_ARRAY, PDHCPV6CAPI_PARAMS_ARRAY structure pointer [DHCP], dhcp.dhcpv6capi_params_array, dhcpv6csdk/DHCPV6CAPI_PARAMS_ARRAY, dhcpv6csdk/LPDHCPV6CAPI_PARAMS_ARRAY, dhcpv6csdk/PDHCPV6CAPI_PARAMS_ARRAY'
req.header: dhcpv6csdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: DHCPV6CAPI_PARAMS_ARRAY, *PDHCPV6CAPI_PARAMS_ARRAY, *LPDHCPV6CAPI_PARAMS_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPV6CAPI_PARAMS_ARRAY
 - dhcpv6csdk/_DHCPV6CAPI_PARAMS_ARRAY
 - PDHCPV6CAPI_PARAMS_ARRAY
 - dhcpv6csdk/PDHCPV6CAPI_PARAMS_ARRAY
 - DHCPV6CAPI_PARAMS_ARRAY
 - dhcpv6csdk/DHCPV6CAPI_PARAMS_ARRAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpv6csdk.h
api_name:
 - DHCPV6CAPI_PARAMS_ARRAY
---

# DHCPV6CAPI_PARAMS_ARRAY structure


## -description

The <b>DHCPV6CAPI_PARAMS_ARRAY</b> structure contains an array of requested parameters.

## -struct-fields

### -field nParams

Number of parameters in the array.

### -field Params

Pointer to a <a href="/windows/desktop/api/dhcpv6csdk/ns-dhcpv6csdk-dhcpv6capi_params">DHCPV6CAPI_PARAMS</a> structure that contains a parameter.