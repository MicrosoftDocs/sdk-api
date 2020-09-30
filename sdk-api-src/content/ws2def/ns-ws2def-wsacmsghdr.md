---
UID: NS:ws2def._WSACMSGHDR
title: WSACMSGHDR (ws2def.h)
description: The CMSGHDR structure defines the header for a control data object that is associated with a datagram.
helpviewer_keywords: ["*LPWSACMSGHDR","*PCMSGHDR","*PWSACMSGHDR","CMSGHDR","CMSGHDR structure [Network Drivers Starting with Windows Vista]","PCMSGHDR","PCMSGHDR structure pointer [Network Drivers Starting with Windows Vista]","WSACMSGHDR","netvista.cmsghdr","ws2def/CMSGHDR","ws2def/PCMSGHDR","wskref_23745253-c7fd-498a-990a-d90d0722d105.xml"]
old-location: netvista\cmsghdr.htm
tech.root: NetVista
ms.assetid: c07dd974-7a23-44c2-b55a-aadfe8936954
ms.date: 12/05/2018
ms.keywords: '*LPWSACMSGHDR, *PCMSGHDR, *PWSACMSGHDR, CMSGHDR, CMSGHDR structure [Network Drivers Starting with Windows Vista], PCMSGHDR, PCMSGHDR structure pointer [Network Drivers Starting with Windows Vista], WSACMSGHDR, netvista.cmsghdr, ws2def/CMSGHDR, ws2def/PCMSGHDR, wskref_23745253-c7fd-498a-990a-d90d0722d105.xml'
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
req.typenames: WSACMSGHDR, *PWSACMSGHDR, *LPWSACMSGHDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSACMSGHDR
 - ws2def/_WSACMSGHDR
 - PWSACMSGHDR
 - ws2def/PWSACMSGHDR
 - WSACMSGHDR
 - ws2def/WSACMSGHDR
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
 - CMSGHDR
---

# WSACMSGHDR structure


## -description

The CMSGHDR structure defines the header for a control data object that is associated with a
  datagram.

## -struct-fields

### -field cmsg_len

The number of bytes from the beginning of the CMSGHDR structure to the end of the control data.

<div class="alert"><b>Note</b>  The value of the 
      <b>cmsg_len</b> member does not account for any padding that may follow the
      control data.</div>
<div> </div>

### -field cmsg_level

The protocol that originated the control information.

### -field cmsg_type

The protocol-specific type of control information.

## -remarks

The control information data that is associated with a datagram is made up of one or more control data
    objects. Each object begins with a CMSGHDR structure.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/wsk/ns-wsk-_wsk_datagram_indication">WSK_DATAGRAM_INDICATION</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_receive_from">WskReceiveFrom</a>



<a href="/windows-hardware/drivers/ddi/content/wsk/nc-wsk-pfn_wsk_send_to">WskSendTo</a>