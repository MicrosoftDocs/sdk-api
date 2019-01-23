---
UID: NF:netcon.NcFreeNetconProperties
title: NcFreeNetconProperties function
author: windows-sdk-content
description: The NcFreeNetconProperties function frees memory associated with NETCON_PROPERTIES structures.
old-location: ics\ncfreenetconproperties.htm
tech.root: ics
ms.assetid: ac73b831-81da-48e7-858b-7ca1ee03768e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NcFreeNetconProperties, NcFreeNetconProperties function [ICS/ICF], ics.ncfreenetconproperties, netcon/NcFreeNetconProperties
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NcFreeNetconProperties function


## -description


<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/4043a85f-ebdc-424c-acf5-9097d1472773">Windows Firewall API</a>.]

The 
<b>NcFreeNetconProperties</b> function frees memory associated with <a href="https://msdn.microsoft.com/en-us/library/Aa366207(v=VS.85).aspx">NETCON_PROPERTIES</a> structures.


## -parameters




### -param pProps [in]

Pointer to a  <a href="https://msdn.microsoft.com/en-us/library/Aa366207(v=VS.85).aspx">NETCON_PROPERTIES</a> structure to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/dfef918e-9abf-4ac2-8365-28cd5b249add">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa366131(v=VS.85).aspx">Internet Connection Sharing and Internet Connection Firewall Reference</a>
 

 

