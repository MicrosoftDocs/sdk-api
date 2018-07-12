---
UID: NF:wdspxe.PxeDhcpv6Initialize
title: PxeDhcpv6Initialize function
author: windows-sdk-content
description: Initializes a response packet as a DHCPv6 reply packet.
old-location: wds\pxedhcpv6initialize.htm
old-project: wds
ms.assetid: B9287BDA-3C7A-457C-8D70-E27A0B9BAE99
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: PxeDhcpv6Initialize, PxeDhcpv6Initialize function [Windows Deployment Services], wds.pxedhcpv6initialize, wdspxe/PxeDhcpv6Initialize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WDS_CLI_CRED, *PWDS_CLI_CRED, *LPWDS_CLI_CRED
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeDhcpv6Initialize
product: Windows
targetos: Windows
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PxeDhcpv6Initialize function


## -description


Initializes a response packet as a DHCPv6 reply packet.

For RELAY-FORW messages, this function initializes the message type, hop count, link address and peer address.  For other DHCPv6 request types, this function initializes the message type and transaction ID.  In all cases, the option payload of the produced packet will be empty.

For more information about RELAY-FORW messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).


## -parameters




### -param pRequest [in]

Address of a valid DHCPv6 packet received from the client in the 
      <a href="https://msdn.microsoft.com/704972d5-177a-490e-881f-d2b3025babda">PxeProviderRecvRequest</a> callback.


### -param cbRequest [in]

Length of the packet pointed to by the <i>pRequest</i> parameter.


### -param pReply [in, out]

Pointer to a reply packet allocated with 
      the <a href="https://msdn.microsoft.com/f3a664a8-565c-4894-bea7-6664df0ecd9b">PxePacketAllocate</a> function.


### -param cbReply [in]

Allocated length of the packet pointed to by the <i>pReply</i> parameter.


### -param pcbReplyUsed [out]

Address of a <b>ULONG</b> that on successful completion will receive the length of 
      the packet pointed to by the <i>pReply</i> parameter.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.



