---
UID: NF:dhcpcsdk.DhcpCApiInitialize
title: DhcpCApiInitialize function (dhcpcsdk.h)
description: The DhcpCApiInitialize function must be the first function call made by users of DHCP; it prepares the system for all other DHCP function calls. Other DHCP functions should only be called if the DhcpCApiInitialize function executes successfully.
helpviewer_keywords: ["DhcpCApiInitialize","DhcpCApiInitialize function [DHCP]","_dhcp_dhcpcapiinitialize","dhcp.dhcpcapiinitialize","dhcpcsdk/DhcpCApiInitialize"]
old-location: dhcp\dhcpcapiinitialize.htm
tech.root: DHCP
ms.assetid: b4bc8b02-63b4-4751-a963-25336e8ae426
ms.date: 12/05/2018
ms.keywords: DhcpCApiInitialize, DhcpCApiInitialize function [DHCP], _dhcp_dhcpcapiinitialize, dhcp.dhcpcapiinitialize, dhcpcsdk/DhcpCApiInitialize
req.header: dhcpcsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpCApiInitialize
 - dhcpcsdk/DhcpCApiInitialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpcsvc.dll
api_name:
 - DhcpCApiInitialize
---

# DhcpCApiInitialize function


## -description

The 
<b>DhcpCApiInitialize</b> function must be the first function call made by users of DHCP; it prepares the system for all other DHCP function calls. Other DHCP functions should only be called if the 
<b>DhcpCApiInitialize</b> function executes successfully.

## -parameters

### -param Version [out]

Pointer to the DHCP version implemented by the client.

## -returns

Returns ERROR_SUCCESS upon successful completion.

## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-functions">DHCP Functions</a>



<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpcapicleanup">DhcpCApiCleanup</a>