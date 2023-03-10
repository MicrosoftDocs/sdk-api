---
UID: NF:iphlpapi.GetUdpTable
title: GetUdpTable function (iphlpapi.h)
description: Retrieves the IPv4 User Datagram Protocol (UDP) listener table.
helpviewer_keywords: ["GetUdpTable","GetUdpTable function [IP Helper]","_iphlp_getudptable","iphlp.getudptable","iphlpapi/GetUdpTable"]
old-location: iphlp\getudptable.htm
tech.root: IpHlp
ms.assetid: 00e80e90-1a6d-426d-90cd-20b967ebbb8e
ms.date: 12/05/2018
ms.keywords: GetUdpTable, GetUdpTable function [IP Helper], _iphlp_getudptable, iphlp.getudptable, iphlpapi/GetUdpTable
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
 - GetUdpTable
 - iphlpapi/GetUdpTable
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
 - GetUdpTable
---

# GetUdpTable function


## -description

The 
<b>GetUdpTable</b> function retrieves the IPv4 User Datagram Protocol (UDP) listener table.

## -parameters

### -param UdpTable [out]

A pointer to a buffer that receives the IPv4 UDP listener table as a 
<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a> structure.

### -param SizePointer [in, out]

On input, specifies the size in bytes of the buffer pointed to by the <i>UdpTable</i> parameter. 




On output, if the buffer is not large enough to hold the returned listener table, the function sets this parameter equal to the required buffer size in bytes.

On the Windows SDK released for Windows Vista and later, the data type for this parameter is changed to a <b>PULONG</b> which is equivalent to a <b>PDWORD</b>.

### -param Order [in]

A Boolean value that specifies whether the returned UDP listener table should be sorted. If this parameter is <b>TRUE</b>, the table is sorted in the order of: 


<ol>
<li>Local IP address</li>
<li>Local port</li>
</ol>

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>pUdpTable</i> parameter is not large enough. The required size is returned in the <b>ULONG</b> variable pointed to by the <i>pdwSize</i> parameter.

This error is also returned if the <i>pUdpTable</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pdwSize</i> parameter is <b>NULL</b>, or 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudptable">GetUdpTable</a> is unable to write to the memory pointed to by the <i>pdwSize</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function is not supported on the operating system in use on the local system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

On the Windows SDK released for Windows Vista and later, the return value from the <b>GetUdpTable</b> function is changed to a data type of <b>ULONG</b> which is equivalent to a <b>DWORD</b>.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromudp6entry">GetOwnerModuleFromUdp6Entry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromudpentry">GetOwnerModuleFromUdpEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudp6table">GetUdp6Table</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatistics">GetUdpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatisticsex">GetUdpStatisticsEx</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow">MIB_UDPROW</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_module">MIB_UDPROW_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_pid">MIB_UDPROW_OWNER_PID</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_module">MIB_UDPTABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_pid">MIB_UDPTABLE_OWNER_PID</a>