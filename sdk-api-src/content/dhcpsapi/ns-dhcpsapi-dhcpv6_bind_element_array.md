---
UID: NS:dhcpsapi._DHCPV6_BIND_ELEMENT_ARRAY
title: DHCPV6_BIND_ELEMENT_ARRAY (dhcpsapi.h)
description: Specifies an array of DHCPV6_BIND_ELEMENT structures that contain DHCPv6 interface bindings.
helpviewer_keywords: ["*LPDHCPV6_BIND_ELEMENT_ARRAY","DHCPV6_BIND_ELEMENT_ARRAY","DHCPV6_BIND_ELEMENT_ARRAY structure [DHCP]","PDHCPV6_BIND_ELEMENT_ARRAY","PDHCPV6_BIND_ELEMENT_ARRAY structure pointer [DHCP]","dhcp.dhcpv6_bind_element_array","dhcpsapi/DHCPV6_BIND_ELEMENT_ARRAY","dhcpsapi/PDHCPV6_BIND_ELEMENT_ARRAY"]
old-location: dhcp\dhcpv6_bind_element_array.htm
tech.root: DHCP
ms.assetid: b78ebdf8-da24-418c-8fe8-aed3047dfdf3
ms.date: 12/05/2018
ms.keywords: '*LPDHCPV6_BIND_ELEMENT_ARRAY, DHCPV6_BIND_ELEMENT_ARRAY, DHCPV6_BIND_ELEMENT_ARRAY structure [DHCP], PDHCPV6_BIND_ELEMENT_ARRAY, PDHCPV6_BIND_ELEMENT_ARRAY structure pointer [DHCP], dhcp.dhcpv6_bind_element_array, dhcpsapi/DHCPV6_BIND_ELEMENT_ARRAY, dhcpsapi/PDHCPV6_BIND_ELEMENT_ARRAY'
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DHCPV6_BIND_ELEMENT_ARRAY, *LPDHCPV6_BIND_ELEMENT_ARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DHCPV6_BIND_ELEMENT_ARRAY
 - dhcpsapi/_DHCPV6_BIND_ELEMENT_ARRAY
 - LPDHCPV6_BIND_ELEMENT_ARRAY
 - dhcpsapi/LPDHCPV6_BIND_ELEMENT_ARRAY
 - DHCPV6_BIND_ELEMENT_ARRAY
 - dhcpsapi/DHCPV6_BIND_ELEMENT_ARRAY
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
 - DHCPV6_BIND_ELEMENT_ARRAY
---

# DHCPV6_BIND_ELEMENT_ARRAY structure


## -description

The <b>DHCPV6_BIND_ELEMENT_ARRAY</b> structure specifies an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_bind_element">DHCPV6_BIND_ELEMENT</a> structures that contain DHCPv6 interface bindings.

## -struct-fields

### -field NumElements

Integer that contains the total number of elements in the array pointed to by <b>Elements</b>.

### -field Elements

Pointer to an array of <a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_bind_element">DHCPV6_BIND_ELEMENT</a> structures that contains the DHCPv6 interface bindings.

### -field Elements.size_is

### -field Elements.size_is.NumElements

## -see-also

<a href="/windows/desktop/api/dhcpsapi/ns-dhcpsapi-dhcpv6_bind_element">DHCPV6_BIND_ELEMENT</a>