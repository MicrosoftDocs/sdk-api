---
UID: NS:wdspxe.tagPXE_ADDRESS
title: PXE_ADDRESS (wdspxe.h)
description: Specifies the network address for a packet.
helpviewer_keywords: ["*PPXE_ADDRESS","PPXE_ADDRESS","PPXE_ADDRESS structure pointer [Windows Deployment Services]","PXE_ADDRESS","PXE_ADDRESS structure [Windows Deployment Services]","PXE_ADDR_BROADCAST","PXE_ADDR_USE_ADDR","PXE_ADDR_USE_DHCP_RULES","PXE_ADDR_USE_PORT","wds.pxe_address","wdspxe/PPXE_ADDRESS","wdspxe/PXE_ADDRESS"]
old-location: wds\pxe_address.htm
tech.root: wds
ms.assetid: ee961e38-331c-4da0-80d1-68d5503f07ea
ms.date: 12/05/2018
ms.keywords: '*PPXE_ADDRESS, PPXE_ADDRESS, PPXE_ADDRESS structure pointer [Windows Deployment Services], PXE_ADDRESS, PXE_ADDRESS structure [Windows Deployment Services], PXE_ADDR_BROADCAST, PXE_ADDR_USE_ADDR, PXE_ADDR_USE_DHCP_RULES, PXE_ADDR_USE_PORT, wds.pxe_address, wdspxe/PPXE_ADDRESS, wdspxe/PXE_ADDRESS'
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
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
req.typenames: PXE_ADDRESS, *PPXE_ADDRESS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagPXE_ADDRESS
 - wdspxe/tagPXE_ADDRESS
 - PPXE_ADDRESS
 - wdspxe/PPXE_ADDRESS
 - PXE_ADDRESS
 - wdspxe/PXE_ADDRESS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WdsPxe.h
api_name:
 - PXE_ADDRESS
---

# PXE_ADDRESS structure


## -description

Specifies the network address for a packet.

## -struct-fields

### -field uFlags

Indicates how the structure should be interpreted and which of the members of the structure are 
      valid.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_ADDR_BROADCAST"></a><a id="pxe_addr_broadcast"></a><dl>
<dt><b>PXE_ADDR_BROADCAST</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
For transmitted packets, this flag specifies that this packet should be broadcast on the network. If the 
        <b>PXE_ADDR_USE_PORT</b> flag is set, then the <b>uPort</b> member 
        specifies the port number to use; otherwise the source port number of the received packet is used as the 
        destination port number. This flag cannot be combined with <b>PXE_ADDR_USE_ADDR</b>.

For received packets, this flag indicates that the packet was set to the server using a broadcast address. 
        The <b>uPort</b> member indicates the port on which the packet was received, in host byte 
        order. The <b>bAddress</b> and <b>uAddrLen</b> members are filled with 
        the broadcast address used.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_ADDR_USE_PORT"></a><a id="pxe_addr_use_port"></a><dl>
<dt><b>PXE_ADDR_USE_PORT</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
For transmitted packets, this flag specifies that the <b>uPort</b> member is valid and 
        should be used as the destination port when the packet is sent. The <b>uPort</b> member 
        must be in host byte order.

For received packets, this flag indicates that the packet was not received as a broadcast.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_ADDR_USE_ADDR"></a><a id="pxe_addr_use_addr"></a><dl>
<dt><b>PXE_ADDR_USE_ADDR</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
For transmitted packets, this flag specifies that the <b>bAddress</b> and 
        <b>uAddrLen</b> members are valid and should be used as the destination address of the 
        packet.

For received packets, this flag is always set.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_ADDR_USE_DHCP_RULES"></a><a id="pxe_addr_use_dhcp_rules"></a><dl>
<dt><b>PXE_ADDR_USE_DHCP_RULES</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
For transmitted packets, this flag specifies that the received packet is a valid DHCP packet, and that the 
        DHCP rules for relay agent should be used to determine the destination address and port. If this flag is 
        specified then <b>bAddress</b>, <b>uIpAddress</b>, 
        <b>uAddrLen</b>, and <b>uPort</b> are ignored.

For received packets, this flag is not used.

</td>
</tr>
</table>

### -field bAddress

Specifies the address of the packet. For more information, see the description for the 
       <b>uFlags</b> member.

### -field uIpAddress

Specifies the IPv4 address. For more information, see the description for the 
       <b>uFlags</b> member.

### -field uAddrLen

Length of the address (<b>bAddress</b> or <b>uIpAddress</b>). For 
      more information, see the description for the <b>uFlags</b> member.

### -field uPort

Port number for the packet. For more information, see the description for the 
      <b>uFlags</b> member.

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxesendreply">PxeSendReply</a>



<a href="/windows/desktop/Wds/windows-deployment-services-structures">Windows Deployment Services Structures</a>