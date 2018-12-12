---
UID: NS:dhcpsapi._DHCP_BIND_ELEMENT_ARRAY
title: DHCP_BIND_ELEMENT_ARRAY
author: windows-sdk-content
description: The DHCP_BIND_ELEMENT_ARRAY structure defines an array of network binding elements used by a DHCP server.
old-location: dhcp\dhcp_bind_element_array.htm
tech.root: DHCP
ms.assetid: 9e43b2ab-f69d-4024-b6b1-8a36a3577767
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDHCP_BIND_ELEMENT_ARRAY, DHCP_BIND_ELEMENT_ARRAY, DHCP_BIND_ELEMENT_ARRAY structure [DHCP], LPDHCP_BIND_ELEMENT_ARRAY, LPDHCP_BIND_ELEMENT_ARRAY structure pointer [DHCP], dhcp.dhcp_bind_element_array, dhcpsapi/LPDHCP_BIND_ELEMENT_ARRAY, dhcpsapi/_DHCP_BIND_ELEMENT_ARRAY"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Dhcpsapi.h
api_name:
 - DHCP_BIND_ELEMENT_ARRAY
product: Windows
targetos: Windows
req.typenames: DHCP_BIND_ELEMENT_ARRAY, *LPDHCP_BIND_ELEMENT_ARRAY
req.redist: 
---

# DHCP_BIND_ELEMENT_ARRAY structure


## -description


The <b>DHCP_BIND_ELEMENT_ARRAY</b> structure defines an array of network binding elements used by a DHCP server.


## -struct-fields




### -field NumElements

Specifies the number of network binding elements listed in <i>Elements</i>.


### -field Elements

Specifies an array of <a href="https://msdn.microsoft.com/00d9d23e-fb39-4f3c-a2b9-9983322879fd">DHCP_BIND_ELEMENT</a> structures


### -field Elements.size_is

 


### -field Elements.size_is.NumElements

 




## -see-also




<a href="https://msdn.microsoft.com/00d9d23e-fb39-4f3c-a2b9-9983322879fd">DHCP_BIND_ELEMENT</a>



<a href="https://msdn.microsoft.com/c0f5c9c1-d421-4977-aa26-1b8b7406802d">DhcpGetServerBindingInfo</a>



<a href="https://msdn.microsoft.com/6291e266-e9d5-4899-8b34-53695f49a1b8">DhcpSetServerBindingInfo</a>
 

 

