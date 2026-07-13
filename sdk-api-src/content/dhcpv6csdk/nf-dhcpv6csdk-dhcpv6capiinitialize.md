---
UID: NF:dhcpv6csdk.Dhcpv6CApiInitialize
title: Dhcpv6CApiInitialize function (dhcpv6csdk.h)
description: The Dhcpv6CApiInitialize function must be the first function call made by users of DHCPv6.
helpviewer_keywords: ["Dhcpv6CApiInitialize","Dhcpv6CApiInitialize function [DHCP]","dhcp.dhcpv6capiinitialize","dhcpv6csdk/Dhcpv6CApiInitialize"]
old-location: dhcp\dhcpv6capiinitialize.htm
tech.root: DHCP
ms.assetid: 4bf74a3d-5674-4bc7-b94c-cf6232bdc8d9
ms.date: 12/05/2018
ms.keywords: Dhcpv6CApiInitialize, Dhcpv6CApiInitialize function [DHCP], dhcp.dhcpv6capiinitialize, dhcpv6csdk/Dhcpv6CApiInitialize
req.header: dhcpv6csdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DhcpCSvc6.Lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Dhcpv6CApiInitialize
 - dhcpv6csdk/Dhcpv6CApiInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dhcpv6csdk.h
api_name:
 - Dhcpv6CApiInitialize
---

# Dhcpv6CApiInitialize function


## -description

The 
<b>Dhcpv6CApiInitialize</b> function must be the first function call made by users of DHCPv6. The function prepares the system for all other DHCPv6 function calls. Other DHCPv6 functions should only be called if the 
<b>Dhcpv6CApiInitialize</b> function executes successfully.

## -parameters

### -param Version [out]

Pointer to the DHCPv6 version implemented by the client.  If a valid pointer is passed, the DHCPv6 client will be returned through it.

## -returns

Returns ERROR_SUCCESS upon successful completion.

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-functions">DHCP Functions</a>



<a href="/previous-versions/windows/desktop/api/dhcpv6csdk/nf-dhcpv6csdk-dhcpv6capicleanup">Dhcpv6CApiCleanup</a>