---
UID: NE:netcon.tagNETCON_TYPE
title: NETCON_TYPE (netcon.h)
description: The NETCON_TYPE type enumerates the various kinds of network connections.
helpviewer_keywords: ["NCT_BRIDGE","NCT_DIRECT_CONNECT","NCT_INBOUND","NCT_INTERNET","NCT_LAN","NCT_PHONE","NCT_TUNNEL","NETCON_TYPE","NETCON_TYPE enumeration [ICS/ICF]","_ics_netcon_type","ics.netcon_type","netcon/NCT_BRIDGE","netcon/NCT_DIRECT_CONNECT","netcon/NCT_INBOUND","netcon/NCT_INTERNET","netcon/NCT_LAN","netcon/NCT_PHONE","netcon/NCT_TUNNEL","netcon/NETCON_TYPE"]
old-location: ics\netcon_type.htm
tech.root: ics
ms.assetid: 7ad507dd-62aa-47c2-a792-750b36d48243
ms.date: 12/05/2018
ms.keywords: NCT_BRIDGE, NCT_DIRECT_CONNECT, NCT_INBOUND, NCT_INTERNET, NCT_LAN, NCT_PHONE, NCT_TUNNEL, NETCON_TYPE, NETCON_TYPE enumeration [ICS/ICF], _ics_netcon_type, ics.netcon_type, netcon/NCT_BRIDGE, netcon/NCT_DIRECT_CONNECT, netcon/NCT_INBOUND, netcon/NCT_INTERNET, netcon/NCT_LAN, netcon/NCT_PHONE, netcon/NCT_TUNNEL, netcon/NETCON_TYPE
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: NETCON_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNETCON_TYPE
 - netcon/tagNETCON_TYPE
 - NETCON_TYPE
 - netcon/NETCON_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NetCon.h
api_name:
 - NETCON_TYPE
---

# NETCON_TYPE enumeration


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>NETCON_TYPE</b> type enumerates the various kinds of network connections.

## -enum-fields

### -field NCT_DIRECT_CONNECT:0

Direct serial connection through a serial port.

### -field NCT_INBOUND:1

Another computer dials in to the local computer through this connection.

### -field NCT_INTERNET

The connection is to the public Internet.

### -field NCT_LAN

The connection is to a local area network (LAN).

### -field NCT_PHONE

The connection is a dial-up connection over a phone line.

### -field NCT_TUNNEL

The connection is a virtual private network (VPN) connection.

### -field NCT_BRIDGE

The connection is a bridged connection.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnection">INetConnection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-enumeration-types">Internet Connection Sharing and Internet Connection Firewall Enumeration Types</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="/windows/desktop/api/netcon/ns-netcon-netcon_properties">NETCON_PROPERTIES</a>
