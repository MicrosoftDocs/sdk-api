---
UID: NF:iphlpapi.GetTcp6Table2
title: GetTcp6Table2 function (iphlpapi.h)
description: Retrieves the TCP connection table for IPv6. (GetTcp6Table2)
helpviewer_keywords: ["GetTcp6Table2","GetTcp6Table2 function [IP Helper]","iphlp.gettcp6table2","iphlpapi/GetTcp6Table2"]
old-location: iphlp\gettcp6table2.htm
tech.root: IpHlp
ms.assetid: 435b9198-b921-407c-9441-31cfe77c03f1
ms.date: 12/05/2018
ms.keywords: GetTcp6Table2, GetTcp6Table2 function [IP Helper], iphlp.gettcp6table2, iphlpapi/GetTcp6Table2
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
 - GetTcp6Table2
 - iphlpapi/GetTcp6Table2
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
 - GetTcp6Table2
---

# GetTcp6Table2 function


## -description

The 
<b>GetTcp6Table2</b> function retrieves the TCP connection table for IPv6.

## -parameters

### -param TcpTable [out]

A pointer to a buffer that receives the TCP connection table for IPv6 as a 
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table2">MIB_TCP6TABLE2</a> structure.

### -param SizePointer [in, out]

On input, specifies the size of the buffer pointed to by the <i>TcpTable</i> parameter. 




On output, if the buffer is not large enough to hold the returned TCP connection table, the function sets this parameter equal to the required buffer size.

### -param Order [in]

A value that specifies whether the TCP connection table should be sorted. If this parameter is <b>TRUE</b>, the table is sorted in ascending order, starting with the lowest local IP address.  If this parameter is <b>FALSE</b>, the table appears in the order in which they were retrieved.

The following values are compared (as listed) when ordering the TCP endpoints:

<ol>
<li>Local IPv6 address</li>
<li>Local scope ID</li>
<li>Local port</li>
<li>Remote IPv6 address</li>
<li>Remote scope ID</li>
<li>Remote port</li>
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
The buffer pointed to by the <i>TcpTable</i> parameter is not large enough. The required size is returned in the variable pointed to by the <i>SizePointer</i> parameter.

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
<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table2">GetTcp6Table2</a> is unable to write to the memory pointed to by the <i>SizePointer</i> parameter.

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

The <b>GetTcp6Table2</b> function is defined on Windows Vista and later. 

The <b>GetTcp6Table2</b> function is an enhanced version of the <a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a> function that also retrieves information on the TCP offload state of the TCP connection.

## -see-also

<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getextendedtcptable">GetExtendedTcpTable</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getownermodulefromtcp6entry">GetOwnerModuleFromTcp6Entry</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcp6table">GetTcp6Table</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcpstatisticsex">GetTcpStatisticsEx</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-gettcptable">GetTcpTable</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row">MIB_TCP6ROW</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row2">MIB_TCP6ROW2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row_owner_module">MIB_TCP6ROW_OWNER_MODULE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6row_owner_pid">MIB_TCP6ROW_OWNER_PID</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table2">MIB_TCP6TABLE2</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_module">MIB_TCP6TABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_pid">MIB_TCP6TABLE_OWNER_PID</a>
