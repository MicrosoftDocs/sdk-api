---
UID: NF:iphlpapi.GetPerAdapterInfo
title: GetPerAdapterInfo function (iphlpapi.h)
description: The GetPerAdapterInfo function retrieves information about the adapter corresponding to the specified interface.
helpviewer_keywords: ["GetPerAdapterInfo","GetPerAdapterInfo function [IP Helper]","_iphlp_getperadapterinfo","iphlp.getperadapterinfo","iphlpapi/GetPerAdapterInfo"]
old-location: iphlp\getperadapterinfo.htm
tech.root: IpHlp
ms.assetid: fc1ae7e4-f856-4b48-8ab4-56cd511ed161
ms.date: 12/05/2018
ms.keywords: GetPerAdapterInfo, GetPerAdapterInfo function [IP Helper], _iphlp_getperadapterinfo, iphlp.getperadapterinfo, iphlpapi/GetPerAdapterInfo
req.header: iphlpapi.h
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
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetPerAdapterInfo
 - iphlpapi/GetPerAdapterInfo
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
 - GetPerAdapterInfo
---

# GetPerAdapterInfo function


## -description

The 
<b>GetPerAdapterInfo</b> function retrieves information about the adapter corresponding to the specified interface.

## -parameters

### -param IfIndex [in]

Index of an interface. 
The <b>GetPerAdapterInfo</b> function retrieves information for the adapter corresponding to this interface.

### -param pPerAdapterInfo [out]

Pointer to an 
<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_per_adapter_info_w2ksp1">IP_PER_ADAPTER_INFO</a> structure that receives information about the adapter.

### -param pOutBufLen [in]

Pointer to a <b>ULONG</b> variable that specifies the size of the 
<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_per_adapter_info_w2ksp1">IP_PER_ADAPTER_INFO</a> structure. If this size is insufficient to hold the information, 
<b>GetPerAdapterInfo</b> fills in this variable with the required size, and returns an error code of ERROR_BUFFER_OVERFLOW.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUFFER_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The buffer size indicated by the <i>pOutBufLen</i> parameter is too small to hold the adapter information. The <i>pOutBufLen</i> parameter points to the required size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pOutBufLen</i> parameter is <b>NULL</b>, or the calling process does not have read/write access to the memory pointed to by <i>pOutBufLen</i>, or the calling process does not have write access to the memory pointed to by the <i>pAdapterInfo</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getperadapterinfo">GetPerAdapterInfo</a> is not supported by the operating system running on the local computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
If the function fails, use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

 An  adapter index  may change when the adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.

## -see-also

<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/IpHlp/ip-helper-start-page">IP Helper Start Page</a>



<a href="/windows/desktop/api/iptypes/ns-iptypes-ip_per_adapter_info_w2ksp1">IP_PER_ADAPTER_INFO</a>