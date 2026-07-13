---
UID: NF:dhcpcsdk.DhcpCApiCleanup
title: DhcpCApiCleanup function (dhcpcsdk.h)
description: The DhcpCApiCleanup function enables DHCP to properly clean up resources allocated throughout the use of DHCP function calls. The DhcpCApiCleanup function must only be called if a previous call to DhcpCApiInitialize executed successfully.
helpviewer_keywords: ["DhcpCApiCleanup","DhcpCApiCleanup function [DHCP]","_dhcp_dhcpcapicleanup","dhcp.dhcpcapicleanup","dhcpcsdk/DhcpCApiCleanup"]
old-location: dhcp\dhcpcapicleanup.htm
tech.root: DHCP
ms.assetid: c1da731c-2e06-40ae-b104-25f144d50c36
ms.date: 12/05/2018
ms.keywords: DhcpCApiCleanup, DhcpCApiCleanup function [DHCP], _dhcp_dhcpcapicleanup, dhcp.dhcpcapicleanup, dhcpcsdk/DhcpCApiCleanup
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
 - DhcpCApiCleanup
 - dhcpcsdk/DhcpCApiCleanup
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
 - DhcpCApiCleanup
---

# DhcpCApiCleanup function


## -description

The 
<b>DhcpCApiCleanup</b> function enables DHCP to properly clean up resources allocated throughout the use of DHCP function calls. The 
<b>DhcpCApiCleanup</b> function must only be called if a previous call to 
<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpcapiinitialize">DhcpCApiInitialize</a> executed successfully.



## -see-also

<a href="/previous-versions/windows/desktop/dhcp/dhcp-functions">DHCP Functions</a>



<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpcapiinitialize">DhcpCApiInitialize</a>
