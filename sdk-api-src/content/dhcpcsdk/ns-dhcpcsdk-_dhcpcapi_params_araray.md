---
UID: NS:dhcpcsdk._DHCPCAPI_PARAMS_ARARAY
title: "_DHCPCAPI_PARAMS_ARARAY"
author: windows-sdk-content
description: The DHCPCAPI_PARAMS_ARRAY structure stores an array of DHCPAPI_PARAMS structures used to query DHCP parameters.
old-location: dhcp\dhcpcapi_params_array.htm
tech.root: DHCP
ms.assetid: 84eafc6b-e9ee-4c73-b872-b2abc7e257df
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*LPDHCPCAPI_PARAMS_ARRAY, *LPDHCPCAPI_PARAMS_ARRAY structure [DHCP], *PDHCPCAPI_PARAMS_ARRAY, *PDHCPCAPI_PARAMS_ARRAY structure [DHCP], DHCPCAPI_PARAMS_ARRAY, DHCPCAPI_PARAMS_ARRAY structure [DHCP], _DHCPCAPI_PARAMS_ARARAY, dhcp.dhcpcapi_params_array, dhcpcsdk/*LPDHCPCAPI_PARAMS_ARRAY, dhcpcsdk/*PDHCPCAPI_PARAMS_ARRAY, dhcpcsdk/DHCPCAPI_PARAMS_ARRAY"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpcsdk.h
api_name:
 - DHCPCAPI_PARAMS_ARRAY
product: Windows
targetos: Windows
req.typenames: DHCPCAPI_PARAMS_ARRAY, *PDHCPCAPI_PARAMS_ARRAY, *LPDHCPCAPI_PARAMS_ARRAY
req.redist: 
---

# _DHCPCAPI_PARAMS_ARARAY structure


## -description


The <b>DHCPCAPI_PARAMS_ARRAY</b> structure stores an array of <a href="https://msdn.microsoft.com/be8329a3-c3ad-4f5b-92ae-cf18fa847d53">DHCPAPI_PARAMS</a> structures used to query DHCP parameters.


## -struct-fields




### -field nParams

Number of elements in the <b>Params</b> array.


### -field Params.size_is

 


### -field Params.size_is.nParams

 


### -field Params

Array of <a href="https://msdn.microsoft.com/be8329a3-c3ad-4f5b-92ae-cf18fa847d53">DHCPAPI_PARAMS</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/be8329a3-c3ad-4f5b-92ae-cf18fa847d53">DHCPAPI_PARAMS</a>
 

 

