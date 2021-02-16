---
UID: NS:dhcpsapi._DHCP_BIND_ELEMENT_ARRAY
title: DHCP_BIND_ELEMENT_ARRAY (dhcpsapi.h)
description: The DHCP_BIND_ELEMENT_ARRAY structure defines an array of network binding elements used by a DHCP server.
helpviewer_keywords: ["*LPDHCP_BIND_ELEMENT_ARRAY","DHCP_BIND_ELEMENT_ARRAY","DHCP_BIND_ELEMENT_ARRAY structure [DHCP]","LPDHCP_BIND_ELEMENT_ARRAY","LPDHCP_BIND_ELEMENT_ARRAY structure pointer [DHCP]","dhcp.dhcp_bind_element_array","dhcpsapi/LPDHCP_BIND_ELEMENT_ARRAY","dhcpsapi/_DHCP_BIND_ELEMENT_ARRAY"]
old-location: dhcp\dhcp_bind_element_array.htm
tech.root: DHCP
ms.assetid: 9e43b2ab-f69d-4024-b6b1-8a36a3577767
ms.date: 12/05/2018
ms.keywords: '*LPDHCP_BIND_ELEMENT_ARRAY, DHCP_BIND_ELEMENT_ARRAY, DHCP_BIND_ELEMENT_ARRAY structure [DHCP], LPDHCP_BIND_ELEMENT_ARRAY, LPDHCP_BIND_ELEMENT_ARRAY structure pointer [DHCP], dhcp.dhcp_bind_element_array, dhcpsapi/LPDHCP_BIND_ELEMENT_ARRAY, dhcpsapi/_DHCP_BIND_ELEMENT_ARRAY'
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
targetos: Windows
req.typenames: DHCP_BIND_ELEMENT_ARRAY, *LPDHCP_BIND_ELEMENT_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCP_BIND_ELEMENT_ARRAY
 - dhcpsapi/_DHCP_BIND_ELEMENT_ARRAY
 - LPDHCP_BIND_ELEMENT_ARRAY
 - dhcpsapi/LPDHCP_BIND_ELEMENT_ARRAY
 - DHCP_BIND_ELEMENT_ARRAY
 - dhcpsapi/DHCP_BIND_ELEMENT_ARRAY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpsapi.h
api_name:
 - DHCP_BIND_ELEMENT_ARRAY
---

# DHCP_BIND_ELEMENT_ARRAY structure


## -description

The <b>DHCP_BIND_ELEMENT_ARRAY</b> structure defines an array of network binding elements used by a DHCP server.

## -struct-fields

### -field NumElements

Specifies the number of network binding elements listed in <i>Elements</i>.

### -field Elements

Specifies an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_bind_element">DHCP_BIND_ELEMENT</a> structures

### -field Elements.size_is

### -field Elements.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcp_bind_element">DHCP_BIND_ELEMENT</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpgetserverbindinginfo">DhcpGetServerBindingInfo</a>



<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpsetserverbindinginfo">DhcpSetServerBindingInfo</a>