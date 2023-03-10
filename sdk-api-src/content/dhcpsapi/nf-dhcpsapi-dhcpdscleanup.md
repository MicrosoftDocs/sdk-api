---
UID: NF:dhcpsapi.DhcpDsCleanup
title: DhcpDsCleanup function (dhcpsapi.h)
description: The DhcpDsCleanup function frees up directory service resources allocated for DHCP services by DhcpDsInit. This function should be called exactly once for each corresponding DHCP service process, and only when the process is terminated.
helpviewer_keywords: ["DhcpDsCleanup","DhcpDsCleanup function [DHCP]","dhcp.dhcpdscleanup","dhcpsapi/DhcpDsCleanup"]
old-location: dhcp\dhcpdscleanup.htm
tech.root: DHCP
ms.assetid: 7d722ca5-a779-4481-b2c7-6d9d7bb5fcfe
ms.date: 12/05/2018
ms.keywords: DhcpDsCleanup, DhcpDsCleanup function [DHCP], dhcp.dhcpdscleanup, dhcpsapi/DhcpDsCleanup
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpDsCleanup
 - dhcpsapi/DhcpDsCleanup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpDsCleanup
---

# DhcpDsCleanup function


## -description

The <b>DhcpDsCleanup</b> function frees up directory service resources allocated for DHCP services by <a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpdsinit">DhcpDsInit</a>. This function should be called exactly once for each corresponding DHCP service process, and only when the process is terminated.



## -see-also

<a href="/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcpdsinit">DhcpDsInit</a>
