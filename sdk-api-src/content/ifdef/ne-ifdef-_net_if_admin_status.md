---
UID: NE:ifdef._NET_IF_ADMIN_STATUS
title: "_NET_IF_ADMIN_STATUS"
author: windows-sdk-content
description: The NET_IF_ADMIN_STATUS enumeration type specifies the NDIS network interface administrative status, as described in RFC 2863.
old-location: netvista\net_if_admin_status.htm
old-project: netvista
ms.assetid: 9f6978a9-a779-49c6-b642-c411fa764972
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: "*PNET_IF_ADMIN_STATUS, NET_IF_ADMIN_STATUS, NET_IF_ADMIN_STATUS enumeration [Network Drivers Starting with Windows Vista], NET_IF_ADMIN_STATUS_DOWN, NET_IF_ADMIN_STATUS_TESTING, NET_IF_ADMIN_STATUS_UP, PNET_IF_ADMIN_STATUS, PNET_IF_ADMIN_STATUS enumeration pointer [Network Drivers Starting with Windows Vista], _NET_IF_ADMIN_STATUS, ifdef/NET_IF_ADMIN_STATUS, ifdef/NET_IF_ADMIN_STATUS_DOWN, ifdef/NET_IF_ADMIN_STATUS_TESTING, ifdef/NET_IF_ADMIN_STATUS_UP, ifdef/PNET_IF_ADMIN_STATUS, net_if_enums_ref_d52428da-7651-4581-8ec4-9409fbfc663f.xml, netvista.net_if_admin_status"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: ifdef.h
req.include-header: Netioapi.h, Ntddndis.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Supported in NDIS 6.0 and later.
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
tech.root: 
req.typenames: NET_IF_ADMIN_STATUS, *PNET_IF_ADMIN_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ifdef.h
api_name:
 - NET_IF_ADMIN_STATUS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _NET_IF_ADMIN_STATUS enumeration


## -description


The NET_IF_ADMIN_STATUS enumeration type specifies the 
  <a href="https://msdn.microsoft.com/library/Ff566527(v=VS.85).aspx">NDIS network interface</a> administrative
  status, as described in RFC 2863.


## -enum-fields




### -field NET_IF_ADMIN_STATUS_UP

Specifies that the interface is initialized and enabled, but the interface is not necessarily
     ready to transmit and receive network data because that depends on the operational status of the
     interface. For more information about the operational status of an interface, see 
     <a href="https://msdn.microsoft.com/library/Ff569619(v=VS.85).aspx">OID_GEN_OPERATIONAL_STATUS</a>.


### -field NET_IF_ADMIN_STATUS_DOWN

Specifies that the interface is down, and this interface cannot be used to transmit or receive
     network data.


### -field NET_IF_ADMIN_STATUS_TESTING

Specifies that the interface is in a test mode, and no network data can be transmitted or
     received.


## -remarks



For more information on RFC 2863, see 
    <a href="http://go.microsoft.com/fwlink/p/?linkid=84054">"The Interfaces Group MIB"</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/Ff569437(v=VS.85).aspx">OID_GEN_ADMIN_STATUS</a>
 

 

