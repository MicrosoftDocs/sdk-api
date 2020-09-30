---
UID: NF:wdspxe.PxeDhcpInitialize
title: PxeDhcpInitialize function (wdspxe.h)
description: Initializes a response packet as a DHCP reply packet.
helpviewer_keywords: ["PxeDhcpInitialize","PxeDhcpInitialize function [Windows Deployment Services]","wds.pxedhcpinitialize","wdspxe/PxeDhcpInitialize"]
old-location: wds\pxedhcpinitialize.htm
tech.root: wds
ms.assetid: b1bcd725-723c-47a3-a2b9-468f5f2e6596
ms.date: 12/05/2018
ms.keywords: PxeDhcpInitialize, PxeDhcpInitialize function [Windows Deployment Services], wds.pxedhcpinitialize, wdspxe/PxeDhcpInitialize
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
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PxeDhcpInitialize
 - wdspxe/PxeDhcpInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeDhcpInitialize
---

# PxeDhcpInitialize function


## -description

Initializes a response packet as a DHCP reply packet.

## -parameters

### -param pRecvPacket [in]

Address of a valid DHCP packet received from the client in the 
      <a href="/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a> callback.

### -param uRecvPacketLen [in]

Length of the packet pointed to by the <i>pRecvPacket</i> parameter.

### -param pReplyPacket [in, out]

Pointer to a reply packet allocated with 
      the <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a> function.

### -param uMaxReplyPacketLen [in]

Allocated length of the packet pointed to by the <i>pReplyPacket</i> parameter.

### -param puReplyPacketLen [out]

Address of a <b>ULONG</b> that on successful completion will receive the length of 
      the packet pointed to by the <i>pReplyPacket</i> parameter.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -remarks

Providers use this function to initialize a reply packet based on the packet received from the client. The 
    reply packet is initialized as follows.

<table>
<tr>
<th>DHCP field</th>
<th>Initialized value</th>
</tr>
<tr>
<td>Operation (op)</td>
<td>2 (BOOTP Reply)</td>
</tr>
<tr>
<td>Hardware Address Type (htype)</td>
<td>Copied from <i>pRecvPacket</i></td>
</tr>
<tr>
<td>Hardware Address Length (hlen)</td>
<td>Copied from <i>pRecvPacket</i></td>
</tr>
<tr>
<td>Hardware Address (chaddr)</td>
<td>Copied from <i>pRecvPacket</i></td>
</tr>
<tr>
<td>Transaction ID (xid)</td>
<td>Copied from <i>pRecvPacket</i></td>
</tr>
<tr>
<td>Seconds Since Boot (secs)</td>
<td>Copied from <i>pRecvPacket</i></td>
</tr>
<tr>
<td>Client IP Address (ciaddr)</td>
<td>Copied from <i>pRecvPacket</i></td>
</tr>
<tr>
<td>Your IP Address (yiaddr)</td>
<td>Copied from <i>pRecvPacket</i></td>
</tr>
<tr>
<td>Server IP Address (siaddr)</td>
<td>Copied from <i>pRecvPacket</i></td>
</tr>
<tr>
<td>Relay Agent IP Address (giaddr)</td>
<td>Copied from <i>pRecvPacket</i></td>
</tr>
<tr>
<td>Magic Cookie (first 4 octets of vend)</td>
<td>Copied from <i>pRecvPacket</i></td>
</tr>
</table>
 

All other fields are initialized to zero.

## -see-also

<a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxepacketallocate">PxePacketAllocate</a>



<a href="/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>