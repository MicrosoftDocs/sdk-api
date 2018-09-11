---
UID: NF:iphlpapi.GetAdapterOrderMap
title: GetAdapterOrderMap function
author: windows-sdk-content
description: The GetAdapterOrderMap function obtains an adapter order map that indicates priority for interfaces on the local computer.
old-location: iphlp\getadapterordermap.htm
tech.root: iphlp
ms.assetid: 43d7429b-6874-4ea6-bbf0-67456af520bc
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: GetAdapterOrderMap, GetAdapterOrderMap function [IP Helper], iphlp.getadapterordermap, iphlpapi/GetAdapterOrderMap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetAdapterOrderMap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetAdapterOrderMap function


## -description


The <b>GetAdapterOrderMap</b> function obtains an adapter order map that indicates priority for interfaces on the local computer.


## -parameters








## -returns



Returns an <a href="https://msdn.microsoft.com/0bbd008e-67d4-4557-bff7-f0404a8878ff">IP_ADAPTER_ORDER_MAP</a> structure filled with adapter priority information.  See the <b>IP_ADAPTER_ORDER_MAP</b> structure for more information.




## -remarks



Interface indices appear in the order specified in the Adapters and Bindings dialog box in the Advanced Settings property sheet. This ordering is used as a tie breaker controlling the sequence in which interfaces are used on multihomed systems for situations including route selection, DNS name resolution, and other network related operations.

This function should not be called directly. Instead, use the <a href="https://msdn.microsoft.com/f8035801-ca0c-4d86-bfc5-8e2d746af1b4">IP_ADAPTER_INFO</a> structure returned in a <a href="https://msdn.microsoft.com/8cdecc84-6566-438b-86d0-3c55490a9a59">GetAdaptersInfo</a> function call.

<div class="alert"><b>Note</b>  The caller is responsible for calling the <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> function to free the array returned by <b>GetAdapterOrderMap</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/8cdecc84-6566-438b-86d0-3c55490a9a59">GetAdaptersInfo</a>



<a href="https://msdn.microsoft.com/f8035801-ca0c-4d86-bfc5-8e2d746af1b4">IP_ADAPTER_INFO</a>



<a href="https://msdn.microsoft.com/0bbd008e-67d4-4557-bff7-f0404a8878ff">IP_ADAPTER_ORDER_MAP</a>



<a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>
 

 

