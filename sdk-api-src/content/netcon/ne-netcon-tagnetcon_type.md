---
UID: NE:netcon.tagNETCON_TYPE
title: tagNETCON_TYPE
author: windows-sdk-content
description: The NETCON_TYPE type enumerates the various kinds of network connections.
old-location: ics\netcon_type.htm
tech.root: ics
ms.assetid: 7ad507dd-62aa-47c2-a792-750b36d48243
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: NCT_BRIDGE, NCT_DIRECT_CONNECT, NCT_INBOUND, NCT_INTERNET, NCT_LAN, NCT_PHONE, NCT_TUNNEL, NETCON_TYPE, NETCON_TYPE enumeration [ICS/ICF], _ics_netcon_type, ics.netcon_type, netcon/NCT_BRIDGE, netcon/NCT_DIRECT_CONNECT, netcon/NCT_INBOUND, netcon/NCT_INTERNET, netcon/NCT_LAN, netcon/NCT_PHONE, netcon/NCT_TUNNEL, netcon/NETCON_TYPE, tagNETCON_TYPE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NetCon.h
api_name:
 - NETCON_TYPE
product: Windows
targetos: Windows
req.typenames: NETCON_TYPE
req.redist: 
---

# tagNETCON_TYPE enumeration


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>NETCON_TYPE</b> type enumerates the various kinds of network connections.


## -enum-fields




### -field NCT_DIRECT_CONNECT

Direct serial connection through a serial port.


### -field NCT_INBOUND

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




<a href="https://msdn.microsoft.com/7dd55645-c8e6-4ebd-9bf6-3bc3b3f5166f">INetConnection</a>



<a href="https://msdn.microsoft.com/fa6cc803-06f5-4b5c-98a5-c37dae08650f">Internet Connection Sharing and Internet Connection Firewall Enumeration Types</a>



<a href="https://msdn.microsoft.com/7ab18626-adc9-450c-a2b8-723d2c839a7b">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="https://msdn.microsoft.com/5acda2b8-960f-41ef-9ff2-49787f4e1c0c">NETCON_PROPERTIES</a>
 

 

