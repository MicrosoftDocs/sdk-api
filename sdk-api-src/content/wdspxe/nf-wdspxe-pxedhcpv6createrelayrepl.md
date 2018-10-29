---
UID: NF:wdspxe.PxeDhcpv6CreateRelayRepl
title: PxeDhcpv6CreateRelayRepl function
author: windows-sdk-content
description: Generates a RELAY-REPL message.
old-location: wds\pxedhcpv6createrelayrepl.htm
tech.root: Wds
ms.assetid: 0FE31279-64CA-4B5E-87E4-6BD035A59A02
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: PxeDhcpv6CreateRelayRepl, PxeDhcpv6CreateRelayRepl function [Windows Deployment Services], wds.pxedhcpv6createrelayrepl, wdspxe/PxeDhcpv6CreateRelayRepl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeDhcpv6CreateRelayRepl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PxeDhcpv6CreateRelayRepl function


## -description


Generates a RELAY-REPL message.

For more information about RELAY-REPL and RELAY-FORW messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).


## -parameters




### -param pRelayMessages [in]

An array of <b>PXE_DHCPV6_NESTED_RELAY_FORW</b> structures which together specify the sequence of nested RELAY-FORW packets.  This value can be obtained from the <i>pRelayMessages</i> parameter of <a href="https://msdn.microsoft.com/1D9F1FFF-3ABB-4580-A5F2-C74B5E7EEAC9">PxeDhcpv6ParseRelayForw</a>.


### -param nRelayMessages [in]

The number of elements in the array pointed to by the <i>pRelayMessages</i> argument.


### -param pInnerPacket [in]

A pointer to a packet which is the server’s response to the innermost packet in the RELAY-FORW chain.


### -param cbInnerPacket [in]

The size of the packet pointed to by the <i>pInnerPacket</i> argument.


### -param pReplyBuffer [out]

A pointer to a buffer used to construct the outer RELAY-REPL packet. This buffer receives the nested response packet and the nested RELAY-REPL chain specified by the <i>pRelayMessages</i> parameter.


### -param cbReplyBuffer [in]

The size of the buffer in bytes  pointed to by <i>pRelyBuffer</i>.


### -param pcbReplyBuffer [out]

On success, this is set to the actual size of the RELAY-REPL packet in the buffer pointed to by <i>pRelyBuffer</i>.  


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.



