---
UID: NF:iphlpapi.GetUdp6Table
title: GetUdp6Table function (iphlpapi.h)
description: Retrieves the IPv6 User Datagram Protocol (UDP) listener table.
helpviewer_keywords: ["GetUdp6Table","GetUdp6Table function [IP Helper]","iphlp.getudp6table","iphlpapi/GetUdp6Table"]
old-location: iphlp\getudp6table.htm
tech.root: IpHlp
ms.assetid: 5e86483c-aa39-4d6c-a9b4-9b046b3dcc74
ms.date: 12/05/2018
ms.keywords: GetUdp6Table, GetUdp6Table function [IP Helper], iphlp.getudp6table, iphlpapi/GetUdp6Table
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - GetUdp6Table
 - iphlpapi/GetUdp6Table
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
 - GetUdp6Table
---

# GetUdp6Table function


## -description

The 
<b>GetUdp6Table</b> function retrieves the IPv6 User Datagram Protocol (UDP) listener table.

## -parameters

### -param Udp6Table [out]

A pointer to a buffer that receives the IPv6 UDP listener table as a 
<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table">MIB_UDP6TABLE</a> structure.

### -param SizePointer [in, out]

On input, specifies the size in bytes of the buffer pointed to by the <i>Udp6Table</i> parameter. 




On output, if the buffer is not large enough to hold the returned listener table, the function sets this parameter equal to the required buffer size in bytes.

### -param Order [in]

A Boolean value that specifies whether the returned UDP listener table should be sorted. If this parameter is <b>TRUE</b>, the table is sorted in the order of: 


<ol>
<li>Local IPv6 address</li>
<li>Local scope ID</li>
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
The buffer pointed to by the <i>Udp6Table</i> parameter is not large enough. The required size is returned in the <b>ULONG</b> variable pointed to by the <i>SizePointer</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>SizePointer</i> parameter is <b>NULL</b>, or 
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudp6table">GetUdp6Table</a> is unable to write to the memory pointed to by the <i>SizePointer</i> parameter.

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

The <b>GetUdp6Table</b> function is defined on Windows Vista and later.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedudptable">GetExtendedUdpTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromudp6entry">GetOwnerModuleFromUdp6Entry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromudpentry">GetOwnerModuleFromUdpEntry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudp6table">GetUdp6Table</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatistics">GetUdpStatistics</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getudpstatisticsex">GetUdpStatisticsEx</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row">MIB_UDP6ROW</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row_owner_module">MIB_UDP6ROW_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6row_owner_pid">MIB_UDP6ROW_OWNER_PID</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table">MIB_UDP6TABLE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_module">MIB_UDP6TABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udp6table_owner_pid">MIB_UDP6TABLE_OWNER_PID</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow">MIB_UDPROW</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_module">MIB_UDPROW_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udprow_owner_pid">MIB_UDPROW_OWNER_PID</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable">MIB_UDPTABLE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_module">MIB_UDPTABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/udpmib/ns-udpmib-mib_udptable_owner_pid">MIB_UDPTABLE_OWNER_PID</a>