---
UID: NS:ws2def.sockaddr
title: SOCKADDR (ws2def.h)
description: The SOCKADDR structure is a generic structure that specifies a transport address.
helpviewer_keywords: ["*LPSOCKADDR","*PSOCKADDR","PSOCKADDR","PSOCKADDR structure pointer [Network Drivers Starting with Windows Vista]","SOCKADDR","SOCKADDR structure [Network Drivers Starting with Windows Vista]","netvista.sockaddr","ws2def/PSOCKADDR","ws2def/SOCKADDR","wskref_4198a308-7f9c-4c7c-ba32-8f11e65e2349.xml"]
old-location: netvista\sockaddr.htm
tech.root: NetVista
ms.assetid: af5ad9ae-3987-4f16-a8a6-14e3e3d0fa6a
ms.date: 12/05/2018
ms.keywords: '*LPSOCKADDR, *PSOCKADDR, PSOCKADDR, PSOCKADDR structure pointer [Network Drivers Starting with Windows Vista], SOCKADDR, SOCKADDR structure [Network Drivers Starting with Windows Vista], netvista.sockaddr, ws2def/PSOCKADDR, ws2def/SOCKADDR, wskref_4198a308-7f9c-4c7c-ba32-8f11e65e2349.xml'
req.header: ws2def.h
req.include-header: Wsk.h
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
req.typenames: SOCKADDR, *PSOCKADDR, *LPSOCKADDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - sockaddr
 - ws2def/sockaddr
 - PSOCKADDR
 - ws2def/PSOCKADDR
 - SOCKADDR
 - ws2def/SOCKADDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ws2def.h
api_name:
 - SOCKADDR
---

# SOCKADDR structure


## -description

The SOCKADDR structure is a generic structure that specifies a transport address.

## -struct-fields

### -field sa_family

The address family for the transport address. For more information about supported address
     families, see 
     <a href="/previous-versions/windows/hardware/drivers/mt808757(v=vs.85)">WSK Address Families</a>.

### -field sa_data

An array of 14 bytes that contains the transport address data.

## -remarks

The SOCKADDR structure is large enough to contain a transport address for most address families. For a
    structure that is guaranteed to be large enough to contain a transport address for all possible address
    families, see 
    [SOCKADDR_STORAGE](./ns-ws2def-sockaddr_storage_lh.md).

A WSK application typically does not access the 
    <b>sa_data</b> member directly. Instead, a pointer to a SOCKADDR structure is normally cast to a pointer
    to the specific SOCKADDR structure type that corresponds to a particular address family.

## -see-also

[SOCKADDR_STORAGE](./ns-ws2def-sockaddr_storage_lh.md)



<a href="/windows-hardware/drivers/ddi/content/wsk/ns-wsk-_wsk_datagram_indication">WSK_DATAGRAM_INDICATION</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_accept">WskAccept</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_accept_event">WskAcceptEvent</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_bind">WskBind</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_connect">WskConnect</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_get_local_address">WskGetLocalAddress</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_get_remote_address">WskGetRemoteAddress</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_inspect_event">WskInspectEvent</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_receive_from">WskReceiveFrom</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_send_to">WskSendTo</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_socket_connect">WskSocketConnect</a>