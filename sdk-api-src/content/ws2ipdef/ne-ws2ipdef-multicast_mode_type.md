---
UID: NE:ws2ipdef.__unnamed_enum_0
title: MULTICAST_MODE_TYPE (ws2ipdef.h)
description: Specifies the filter mode for multicast group addresses.
helpviewer_keywords: ["MCAST_EXCLUDE","MCAST_INCLUDE","MULTICAST_MODE_TYPE","MULTICAST_MODE_TYPE enumeration [Winsock]","winsock.multicast_mode_type","ws2ipdef/MCAST_EXCLUDE","ws2ipdef/MCAST_INCLUDE","ws2ipdef/MULTICAST_MODE_TYPE"]
old-location: winsock\multicast_mode_type.htm
tech.root: WinSock
ms.assetid: 7ca9cb9b-618a-4e73-9e2a-18e55e5c00c0
ms.date: 12/05/2018
ms.keywords: MCAST_EXCLUDE, MCAST_INCLUDE, MULTICAST_MODE_TYPE, MULTICAST_MODE_TYPE enumeration [Winsock], winsock.multicast_mode_type, ws2ipdef/MCAST_EXCLUDE, ws2ipdef/MCAST_INCLUDE, ws2ipdef/MULTICAST_MODE_TYPE
req.header: ws2ipdef.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MULTICAST_MODE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MULTICAST_MODE_TYPE
 - ws2ipdef/MULTICAST_MODE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ws2ipdef.h
api_name:
 - MULTICAST_MODE_TYPE
---

# MULTICAST_MODE_TYPE enumeration


## -description

The <b>MULTICAST_MODE_TYPE</b> enumeration specifies the filter mode for multicast group addresses.

## -enum-fields

### -field MCAST_INCLUDE:0

The filter contains a list of IP addresses to include.

### -field MCAST_EXCLUDE

The filter contains a list of IP addresses to exclude.

## -remarks

This enumeration is supported on Windows Vista and later.

The <b>MULTICAST_MODE_TYPE</b> enumeration is used in the <b>gf_fmode</b> member of the <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-group_source_req">GROUP_SOURCE_REQ</a> structure to determine if a list of IP addresses should included or excluded. The values from this enumeration can also be used in the <b>imsf_fmode</b> member of the <a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ip_msfilter">ip_msfilter</a> structure.

The <b>MULTICAST_MODE_TYPE</b> enumeration is defined in the <i>Ws2ipdef.h</i> header file which is automatically included in the <i>Ws2tcpip.h</i> header file. The <i>Ws2ipdef.h</i>  header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-group_req">GROUP_REQ</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-group_source_req">GROUP_SOURCE_REQ</a>



<a href="/windows/desktop/WinSock/multicast-programming">Multicast Programming</a>



<a href="/windows/desktop/WinSock/socket-options">Socket Options</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ip_mreq">ip_mreq</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ip_msfilter">ip_msfilter</a>



<a href="/windows/desktop/api/ws2ipdef/ns-ws2ipdef-ipv6_mreq">ipv6_mreq</a>
