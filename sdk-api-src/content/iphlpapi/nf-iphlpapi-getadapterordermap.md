---
UID: NF:iphlpapi.GetAdapterOrderMap
title: GetAdapterOrderMap function (iphlpapi.h)
author: windows-sdk-content
description: The GetAdapterOrderMap function obtains an adapter order map that indicates priority for interfaces on the local computer.
old-location: iphlp\getadapterordermap.htm
tech.root: IpHlp
ms.assetid: 43d7429b-6874-4ea6-bbf0-67456af520bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAdapterOrderMap, GetAdapterOrderMap function [IP Helper], iphlp.getadapterordermap, iphlpapi/GetAdapterOrderMap
ms.topic: function
f1_keywords: ["iphlpapi/GetAdapterOrderMap"]
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
ms.custom: 19H1
---

# GetAdapterOrderMap function


## -description


The <b>GetAdapterOrderMap</b> function obtains an adapter order map that indicates priority for interfaces on the local computer.


## -parameters








## -returns



Returns an <a href="https://docs.microsoft.com/windows/desktop/api/ipexport/ns-ipexport-_ip_adapter_order_map">IP_ADAPTER_ORDER_MAP</a> structure filled with adapter priority information.  See the <b>IP_ADAPTER_ORDER_MAP</b> structure for more information.




## -remarks



Interface indices appear in the order specified in the Adapters and Bindings dialog box in the Advanced Settings property sheet. This ordering is used as a tie breaker controlling the sequence in which interfaces are used on multihomed systems for situations including route selection, DNS name resolution, and other network related operations.

This function should not be called directly. Instead, use the <a href="https://docs.microsoft.com/windows/desktop/api/iptypes/ns-iptypes-_ip_adapter_info">IP_ADAPTER_INFO</a> structure returned in a <a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a> function call.

<div class="alert"><b>Note</b>  The caller is responsible for calling the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function to free the array returned by <b>GetAdapterOrderMap</b>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iptypes/ns-iptypes-_ip_adapter_info">IP_ADAPTER_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipexport/ns-ipexport-_ip_adapter_order_map">IP_ADAPTER_ORDER_MAP</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>
 

 

