---
UID: NS:dhcpv6csdk._DHCPV6CAPI_PARAMS_ARRAY
title: "_DHCPV6CAPI_PARAMS_ARRAY"
author: windows-driver-content
description: Contains an array of requested parameters.
old-location: dhcp\dhcpv6capi_params_array.htm
old-project: DHCP
ms.assetid: 2392586f-94a0-4667-b59a-88c0e1d88713
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: "*LPDHCPV6CAPI_PARAMS_ARRAY, *PDHCPV6CAPI_PARAMS_ARRAY, DHCPV6CAPI_PARAMS_ARRAY, DHCPV6CAPI_PARAMS_ARRAY structure [DHCP], LPDHCPV6CAPI_PARAMS_ARRAY, LPDHCPV6CAPI_PARAMS_ARRAY structure pointer [DHCP], PDHCPV6CAPI_PARAMS_ARRAY, PDHCPV6CAPI_PARAMS_ARRAY structure pointer [DHCP], _DHCPV6CAPI_PARAMS_ARRAY, dhcp.dhcpv6capi_params_array, dhcpv6csdk/DHCPV6CAPI_PARAMS_ARRAY, dhcpv6csdk/LPDHCPV6CAPI_PARAMS_ARRAY, dhcpv6csdk/PDHCPV6CAPI_PARAMS_ARRAY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpv6csdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DHCPV6CAPI_PARAMS_ARRAY, *PDHCPV6CAPI_PARAMS_ARRAY, *LPDHCPV6CAPI_PARAMS_ARRAY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dhcpv6csdk.h
api_name:
-	DHCPV6CAPI_PARAMS_ARRAY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DHCPV6CAPI_PARAMS_ARRAY structure


## -description


The <b>DHCPV6CAPI_PARAMS_ARRAY</b> structure contains an array of requested parameters.


## -struct-fields




### -field nParams

Number of parameters in the array.


### -field Params

Pointer to a <a href="https://msdn.microsoft.com/a8978435-a16d-446d-9bd3-4a2dc6c9ec1a">DHCPV6CAPI_PARAMS</a> structure that contains a parameter.

