---
UID: NE:netcon.tagNETCON_MEDIATYPE
title: NETCON_MEDIATYPE (netcon.h)
author: windows-sdk-content
description: The values of the NETCON_MEDIATYPE enumerate the possible ways the computer connects to the network.
old-location: ics\netcon_mediatype.htm
tech.root: ics
ms.assetid: 9236371c-0e3f-43ba-a02f-0770768008ae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NCM_BRIDGE, NCM_DIRECT, NCM_ISDN, NCM_LAN, NCM_NONE, NCM_PHONE, NCM_PPPOE, NCM_SHAREDACCESSHOST_LAN, NCM_SHAREDACCESSHOST_RAS, NCM_TUNNEL, NETCON_MEDIATYPE, NETCON_MEDIATYPE enumeration [ICS/ICF], _ics_netcon_mediatype, ics.netcon_mediatype, netcon/NCM_BRIDGE, netcon/NCM_DIRECT, netcon/NCM_ISDN, netcon/NCM_LAN, netcon/NCM_NONE, netcon/NCM_PHONE, netcon/NCM_PPPOE, netcon/NCM_SHAREDACCESSHOST_LAN, netcon/NCM_SHAREDACCESSHOST_RAS, netcon/NCM_TUNNEL, netcon/NETCON_MEDIATYPE
ms.topic: enum
f1_keywords: 
 - "netcon/NETCON_MEDIATYPE"
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
 - NETCON_MEDIATYPE
product: Windows
targetos: Windows
req.typenames: NETCON_MEDIATYPE
req.redist: 
ms.custom: 19H1
---

# NETCON_MEDIATYPE enumeration


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The values of the <b>NETCON_MEDIATYPE</b> enumerate the possible ways the computer connects to the network.


## -enum-fields




### -field NCM_NONE

No media is present.


### -field NCM_DIRECT

Direct serial connection through a serial port.


### -field NCM_ISDN

Connection is through an integrated services digital network (ISDN) line.


### -field NCM_LAN

Connection is to a local area network (LAN).


### -field NCM_PHONE

Dial-up connection over a conventional phone line.


### -field NCM_TUNNEL

Virtual private network (VPN) connection.


### -field NCM_PPPOE

Point-to-Point protocol (PPP) over Ethernet.


### -field NCM_BRIDGE

Bridged connection.


### -field NCM_SHAREDACCESSHOST_LAN

Shared connection to a LAN.


### -field NCM_SHAREDACCESSHOST_RAS

Shared connection to a remote or wide area network (WAN).


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnection">INetConnection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-enumeration-types">Internet Connection Sharing and Internet Connection Firewall Enumeration Types</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/netcon/ns-netcon-tagnetcon_properties">NETCON_PROPERTIES</a>
 

 

