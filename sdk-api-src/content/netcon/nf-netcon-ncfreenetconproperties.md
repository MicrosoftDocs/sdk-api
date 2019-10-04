---
UID: NF:netcon.NcFreeNetconProperties
title: NcFreeNetconProperties function (netcon.h)
author: windows-sdk-content
description: The NcFreeNetconProperties function frees memory associated with NETCON_PROPERTIES structures.
old-location: ics\ncfreenetconproperties.htm
tech.root: ics
ms.assetid: ac73b831-81da-48e7-858b-7ca1ee03768e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: NcFreeNetconProperties, NcFreeNetconProperties function [ICS/ICF], ics.ncfreenetconproperties, netcon/NcFreeNetconProperties
ms.topic: function
f1_keywords: 
 - "netcon/NcFreeNetconProperties"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netshell.dll
api_name:
 - NcFreeNetconProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NcFreeNetconProperties function


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>NcFreeNetconProperties</b> function frees memory associated with <a href="https://docs.microsoft.com/windows/desktop/api/netcon/ns-netcon-netcon_properties">NETCON_PROPERTIES</a> structures.


## -parameters




### -param pProps [in]

Pointer to a  <a href="https://docs.microsoft.com/windows/desktop/api/netcon/ns-netcon-netcon_properties">NETCON_PROPERTIES</a> structure to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

