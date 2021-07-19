---
UID: NF:iphlpapi.GetAdapterOrderMap
title: GetAdapterOrderMap function (iphlpapi.h)
description: The GetAdapterOrderMap function obtains an adapter order map that indicates priority for interfaces on the local computer.
helpviewer_keywords: ["GetAdapterOrderMap","GetAdapterOrderMap function [IP Helper]","iphlp.getadapterordermap","iphlpapi/GetAdapterOrderMap"]
old-location: iphlp\getadapterordermap.htm
tech.root: IpHlp
ms.assetid: 43d7429b-6874-4ea6-bbf0-67456af520bc
ms.date: 12/05/2018
ms.keywords: GetAdapterOrderMap, GetAdapterOrderMap function [IP Helper], iphlp.getadapterordermap, iphlpapi/GetAdapterOrderMap
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAdapterOrderMap
 - iphlpapi/GetAdapterOrderMap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetAdapterOrderMap
---

# GetAdapterOrderMap function


## -description

The <b>GetAdapterOrderMap</b> function obtains an adapter order map that indicates priority for interfaces on the local computer.



## -returns

Returns an <a href="/windows/desktop/api/ipexport/ns-ipexport-ip_adapter_order_map">IP_ADAPTER_ORDER_MAP</a> structure filled with adapter priority information.  See the <b>IP_ADAPTER_ORDER_MAP</b> structure for more information.

## -remarks

Interface indices appear in the order specified in the Adapters and Bindings dialog box in the Advanced Settings property sheet. This ordering is used as a tie breaker controlling the sequence in which interfaces are used on multihomed systems for situations including route selection, DNS name resolution, and other network related operations.

This function should not be called directly. Instead, use the <a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_info">IP_ADAPTER_INFO</a> structure returned in a <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a> function call.

<div class="alert"><b>Note</b>  The caller is responsible for calling the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function to free the array returned by <b>GetAdapterOrderMap</b>.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_info">IP_ADAPTER_INFO</a>



<a href="/windows/desktop/api/ipexport/ns-ipexport-ip_adapter_order_map">IP_ADAPTER_ORDER_MAP</a>



<a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>
