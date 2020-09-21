---
UID: NF:iphlpapi.GetAdapterIndex
title: GetAdapterIndex function (iphlpapi.h)
description: The GetAdapterIndex function obtains the index of an adapter, given its name.
helpviewer_keywords: ["GetAdapterIndex","GetAdapterIndex function [IP Helper]","_iphlp_getadapterindex","iphlp.getadapterindex","iphlpapi/GetAdapterIndex"]
old-location: iphlp\getadapterindex.htm
tech.root: IpHlp
ms.assetid: e98ee6b3-30c2-4629-859e-e7440781cd86
ms.date: 12/05/2018
ms.keywords: GetAdapterIndex, GetAdapterIndex function [IP Helper], _iphlp_getadapterindex, iphlp.getadapterindex, iphlpapi/GetAdapterIndex
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetAdapterIndex
 - iphlpapi/GetAdapterIndex
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
 - GetAdapterIndex
---

# GetAdapterIndex function


## -description

The 
<b>GetAdapterIndex</b> function obtains the index of an adapter, given its name.

## -parameters

### -param AdapterName [in]

A pointer to a Unicode string that specifies the name of the adapter.

### -param IfIndex [in, out]

A pointer to a <b>ULONG</b> variable that points to the index of the adapter.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

## -remarks

Until an adapter is fully disabled, the <b>GetAdapterIndex</b> function reports the adapter as present. For example, the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyaddrchange">NotifyAddrChange</a> function may indicate a recently disabled adapter's IP address is removed, but <b>GetAdapterIndex</b> continues to report an adapter  index until the process of disabling the adapter is complete.

When one or more adapters are present on the system, <b>GetAdapterIndex</b>  returns ERROR_DEV_NOT_EXIST when the adapter being queried does not exist. When no adapters are present, the <b>GetAdapterIndex</b> function returns ERROR_NO_DATA.

 The adapter index  may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersinfo">GetAdaptersInfo</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_info">IP_ADAPTER_INFO</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiggetfriendlyname">MprConfigGetFriendlyName</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiggetguidname">MprConfigGetGuidName</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-notifyaddrchange">NotifyAddrChange</a>