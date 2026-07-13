---
UID: NF:dhcpv6csdk.Dhcpv6CApiCleanup
title: Dhcpv6CApiCleanup function (dhcpv6csdk.h)
description: The Dhcpv6CApiCleanup function enables DHCPv6 to properly clean up resources allocated throughout the use of DHCPv6 function calls. The Dhcpv6CApiCleanup function must only be called if a previous call to Dhcpv6CApiInitialize executed successfully.
helpviewer_keywords: ["Dhcpv6CApiCleanup","Dhcpv6CApiCleanup function [DHCP]","dhcp.dhcpv6capicleanup","dhcpv6csdk/Dhcpv6CApiCleanup"]
old-location: dhcp\dhcpv6capicleanup.htm
tech.root: DHCP
ms.assetid: eb951723-4bfb-4eb5-85bd-d469163d72e1
ms.date: 12/05/2018
ms.keywords: Dhcpv6CApiCleanup, Dhcpv6CApiCleanup function [DHCP], dhcp.dhcpv6capicleanup, dhcpv6csdk/Dhcpv6CApiCleanup
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
 - Dhcpv6CApiCleanup
 - dhcpv6csdk/Dhcpv6CApiCleanup
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
 - Dhcpv6CApiCleanup
---

# Dhcpv6CApiCleanup function


## -description

The 
<b>Dhcpv6CApiCleanup</b> function enables DHCPv6 to properly clean up resources allocated throughout the use of DHCPv6 function calls. The 
<b>Dhcpv6CApiCleanup</b> function must only be called if a previous call to 
<a href="/previous-versions/windows/desktop/api/dhcpv6csdk/nf-dhcpv6csdk-dhcpv6capiinitialize">Dhcpv6CApiInitialize</a> executed successfully.



## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-functions">DHCP Functions</a>



<a href="/previous-versions/windows/desktop/api/dhcpv6csdk/nf-dhcpv6csdk-dhcpv6capiinitialize">Dhcpv6CApiInitialize</a>
