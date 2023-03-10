---
UID: NF:wdspxe.PxeDhcpv6ParseRelayForw
title: PxeDhcpv6ParseRelayForw function (wdspxe.h)
description: This function can be used by a provider to parse RELAY-FORW messages and their nested OPTION_RELAY_MSG messages.
helpviewer_keywords: ["PxeDhcpv6ParseRelayForw","PxeDhcpv6ParseRelayForw function [Windows Deployment Services]","wds.pxedhcpv6parserelayforw","wdspxe/PxeDhcpv6ParseRelayForw"]
old-location: wds\pxedhcpv6parserelayforw.htm
tech.root: wds
ms.assetid: 1D9F1FFF-3ABB-4580-A5F2-C74B5E7EEAC9
ms.date: 12/05/2018
ms.keywords: PxeDhcpv6ParseRelayForw, PxeDhcpv6ParseRelayForw function [Windows Deployment Services], wds.pxedhcpv6parserelayforw, wdspxe/PxeDhcpv6ParseRelayForw
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PxeDhcpv6ParseRelayForw
 - wdspxe/PxeDhcpv6ParseRelayForw
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
 - PxeDhcpv6ParseRelayForw
---

# PxeDhcpv6ParseRelayForw function


## -description

This function can be used by a provider to parse RELAY-FORW messages and their nested OPTION_RELAY_MSG messages.   The information returned can be used to construct a RELAY-REPL packet using the <a href="/windows/desktop/api/wdspxe/nf-wdspxe-pxedhcpv6createrelayrepl">PxeDhcpv6CreateRelayRepl</a> function.  

For more information about RELAY-FORW and OPTION_RELAY_MSG messages, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="https://www.ietf.org/rfc/rfc3315.txt">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).

## -parameters

### -param pRelayForwPacket [in]

Specifies a pointer to a DHCPv6 RELAY-FORW message.

### -param uRelayForwPacketLen [in]

The size in bytes of the RELAY-FORW message pointed to by the <i>pRelayForwPacket</i> parameter.

### -param pRelayMessages [out]

An array of <a href="/windows/desktop/api/wdspxe/ns-wdspxe-pxe_dhcpv6_nested_relay_message">PXE_DHCPV6_NESTED_RELAY_MESSAGE</a> structures initialized by this routine.  The array’s size is specified by <i>nRelayMessages</i>.  Elements of this array are initialized to point to the nested chain of relay packets encoded in OPTION_RELAY_MSG.  Index 0 is the outermost nested OPTION_RELAY_MSG packet. As the index increases the pointers correspond to more deeply nested OPTION_RELAY_MSG packets.

### -param nRelayMessages [in]

The size of the array, in number of array elements, pointed to by the <i>pRelayMessages</i> parameter.

### -param pnRelayMessages [out]

Specifies a pointer to a <b>ULONG</b> value which on success receives the actual number of elements written into the <i>pRelayMessages</i> array.

### -param ppInnerPacket [out]

Specifies a pointer to a <b>PVOID</b> value which on success is set to the start of the innermost packet in the relay chain. This is the original client request packet.

### -param pcbInnerPacket [out]

Specifies a pointer to a <b>ULONG</b> value which on success will be set to the size, in bytes, of the innermost packet in the relay chain which is the original client request packet.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.