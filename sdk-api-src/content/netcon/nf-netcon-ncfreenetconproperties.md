---
UID: NF:netcon.NcFreeNetconProperties
title: NcFreeNetconProperties function (netcon.h)
description: The NcFreeNetconProperties function frees memory associated with NETCON_PROPERTIES structures.
helpviewer_keywords: ["NcFreeNetconProperties","NcFreeNetconProperties function [ICS/ICF]","ics.ncfreenetconproperties","netcon/NcFreeNetconProperties"]
old-location: ics\ncfreenetconproperties.htm
tech.root: ics
ms.assetid: ac73b831-81da-48e7-858b-7ca1ee03768e
ms.date: 12/05/2018
ms.keywords: NcFreeNetconProperties, NcFreeNetconProperties function [ICS/ICF], ics.ncfreenetconproperties, netcon/NcFreeNetconProperties
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Netshell.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NcFreeNetconProperties
 - netcon/NcFreeNetconProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-net-netshell-l1-1-0.dll
 - Netshell.dll
api_name:
 - NcFreeNetconProperties
---

# NcFreeNetconProperties function


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>NcFreeNetconProperties</b> function frees memory associated with <a href="/windows/desktop/api/netcon/ns-netcon-netcon_properties">NETCON_PROPERTIES</a> structures.

## -parameters

### -param pProps [in]

Pointer to a  <a href="/windows/desktop/api/netcon/ns-netcon-netcon_properties">NETCON_PROPERTIES</a> structure to be freed.

## -see-also

<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>