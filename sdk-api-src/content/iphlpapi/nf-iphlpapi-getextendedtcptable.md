---
UID: NF:iphlpapi.GetExtendedTcpTable
title: GetExtendedTcpTable function (iphlpapi.h)
description: Retrieves a table that contains a list of TCP endpoints available to the application.
helpviewer_keywords: ["AF_INET","AF_INET6","GetExtendedTcpTable","GetExtendedTcpTable function [IP Helper]","iphlp.getextendedtcptable","iphlpapi/GetExtendedTcpTable"]
old-location: iphlp\getextendedtcptable.htm
tech.root: IpHlp
ms.assetid: 96356a0e-ae0d-4000-9223-a578cbdeaa8b
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, GetExtendedTcpTable, GetExtendedTcpTable function [IP Helper], iphlp.getextendedtcptable, iphlpapi/GetExtendedTcpTable
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps \| UWP apps]
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
 - GetExtendedTcpTable
 - iphlpapi/GetExtendedTcpTable
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
 - GetExtendedTcpTable
---

# GetExtendedTcpTable function


## -description

The <b>GetExtendedTcpTable</b> function retrieves a table that contains a list of TCP endpoints available to the application.

## -parameters

### -param pTcpTable [out]

A pointer to the table structure that contains the filtered TCP endpoints available to the application. For information about how to determine the type of table returned based on specific input parameter combinations, see the Remarks section later in this document.

### -param pdwSize [in, out]

The estimated size of the structure returned in <i>pTcpTable</i>, in bytes. If this value is set too small, <b>ERROR_INSUFFICIENT_BUFFER</b> is returned by this function, and this field will contain the correct size of the structure.

### -param bOrder [in]

A value that specifies whether the TCP connection table should be sorted. If this parameter is set to <b>TRUE</b>, the TCP endpoints in the table are sorted in ascending order, starting with the lowest local IP address. If this parameter is set to <b>FALSE</b>, the TCP endpoints in the table appear in the order in which they were retrieved.

The following values are compared (as listed) when ordering the TCP endpoints:<ol>
<li>Local IP address</li>
<li>Local scope ID (applicable when the <i>ulAf</i> parameter is set to AF_INET6)</li>
<li>Local TCP port</li>
<li>Remote IP address</li>
<li>Remote scope ID (applicable when the <i>ulAf</i> parameter is set to AF_INET6)</li>
<li>Remote TCP port</li>
</ol>

### -param ulAf [in]

The version of IP used by the TCP endpoints.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
</dl>
</td>
<td width="60%">
IPv4 is used.

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
</dl>
</td>
<td width="60%">
IPv6 is used.

</td>
</tr>
</table>

### -param TableClass [in]

The type of the TCP table structure to retrieve. This parameter can be one of the values from the <a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-tcp_table_class">TCP_TABLE_CLASS</a> enumeration. 

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the <a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-tcp_table_class">TCP_TABLE_CLASS</a> enumeration is defined in the <i>Iprtrmib.h</i> header file, not in the <i>Iphlpapi.h</i> header file. 

The <a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-tcp_table_class">TCP_TABLE_CLASS</a> enumeration value is combined with the value of the <i>ulAf</i> parameter to determine the extended TCP information to retrieve.

### -param Reserved [in]

Reserved. This value must be zero.

## -returns

If the call is successful, the value <b>NO_ERROR</b> is returned. 

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
An insufficient amount of space was allocated for the table. The size of the table is returned in the <i>pdwSize</i> parameter, and must be used in a subsequent call to this function in order to successfully retrieve the table.

This error is also returned if the <i>pTcpTable</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if the <i>TableClass</i> parameter contains a value that is not defined in the <a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-tcp_table_class">TCP_TABLE_CLASS</a> enumeration.

</td>
</tr>
</table>

## -remarks

The table type returned by this function depends on the specific combination of the <i>ulAf</i> parameter and the <i>TableClass</i> parameter. 

When the <i>ulAf</i> parameter is set to <b>AF_INET</b>, the following table indicates the TCP table type to retrieve in the structure pointed to by the <i>pTcpTable</i> parameter for each possible <i>TableClass</i> value.


<table>
<tr>
<th><i>TableClass</i> value</th>
<th><i>pTcpTable</i> structure</th>
</tr>
<tr>
<td><b>TCP_TABLE_BASIC_ALL</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_BASIC_CONNECTIONS</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_BASIC_LISTENER</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_MODULE_ALL</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_module">MIB_TCPTABLE_OWNER_MODULE</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_MODULE_CONNECTIONS</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_module">MIB_TCPTABLE_OWNER_MODULE</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_MODULE_LISTENER</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_module">MIB_TCPTABLE_OWNER_MODULE</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_PID_ALL</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_pid">MIB_TCPTABLE_OWNER_PID</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_PID_CONNECTIONS</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_pid">MIB_TCPTABLE_OWNER_PID</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_PID_LISTENER</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_pid">MIB_TCPTABLE_OWNER_PID</a>
</td>
</tr>
</table>
 



 When the <i>ulAf</i> parameter is set to <b>AF_INET6</b>, the following table indicates the TCP table type to retrieve in the structure pointed to by the <i>pTcpTable</i> parameter for each possible <i>TableClass</i> value.


<table>
<tr>
<th><i>TableClass</i> value</th>
<th><i>pTcpTable</i> structure</th>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_MODULE_ALL</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_module">MIB_TCP6TABLE_OWNER_MODULE</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_MODULE_CONNECTIONS</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_module">MIB_TCP6TABLE_OWNER_MODULE</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_MODULE_LISTENER</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_module">MIB_TCP6TABLE_OWNER_MODULE</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_PID_ALL</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_pid">MIB_TCP6TABLE_OWNER_PID</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_PID_CONNECTIONS</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_pid">MIB_TCP6TABLE_OWNER_PID</a>
</td>
</tr>
<tr>
<td><b>TCP_TABLE_OWNER_PID_LISTENER</b></td>
<td>
<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_pid">MIB_TCP6TABLE_OWNER_PID</a>
</td>
</tr>
</table>
 



The <b>GetExtendedTcpTable</b> function called with the <i>ulAf</i> parameter set to <b>AF_INET6</b> and the <i>TableClass</i> set to <b>TCP_TABLE_BASIC_LISTENER</b>, <b>TCP_TABLE_BASIC_CONNECTIONS</b>, or <b>TCP_TABLE_BASIC_ALL</b> is not supported and returns <b>ERROR_NOT_SUPPORTED</b>. 

On the Windows SDK released for Windows Vista and later, the organization of header files has changed. The various <a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a> structures are defined in the <i>Tcpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Tcpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The <i>Tcpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.

## -see-also

<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table">MIB_TCP6TABLE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_module">MIB_TCP6TABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcp6table_owner_pid">MIB_TCP6TABLE_OWNER_PID</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable">MIB_TCPTABLE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_module">MIB_TCPTABLE_OWNER_MODULE</a>



<a href="/windows/desktop/api/tcpmib/ns-tcpmib-mib_tcptable_owner_pid">MIB_TCPTABLE_OWNER_PID</a>



<a href="/windows/desktop/api/iprtrmib/ne-iprtrmib-tcp_table_class">TCP_TABLE_CLASS</a>