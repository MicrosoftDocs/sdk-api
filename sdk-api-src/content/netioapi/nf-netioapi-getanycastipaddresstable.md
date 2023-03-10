---
UID: NF:netioapi.GetAnycastIpAddressTable
title: GetAnycastIpAddressTable function (netioapi.h)
description: Retrieves the anycast IP address table on the local computer.
helpviewer_keywords: ["AF_INET","AF_INET6","AF_UNSPEC","GetAnycastIpAddressTable","GetAnycastIpAddressTable function [IP Helper]","iphlp.getanycastipaddresstable","netioapi/GetAnycastIpAddressTable"]
old-location: iphlp\getanycastipaddresstable.htm
tech.root: IpHlp
ms.assetid: 4eccae59-00be-4f9c-bb62-a507d7dad2e0
ms.date: 12/05/2018
ms.keywords: AF_INET, AF_INET6, AF_UNSPEC, GetAnycastIpAddressTable, GetAnycastIpAddressTable function [IP Helper], iphlp.getanycastipaddresstable, netioapi/GetAnycastIpAddressTable
req.header: netioapi.h
req.include-header: Iphlpapi.h
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
 - GetAnycastIpAddressTable
 - netioapi/GetAnycastIpAddressTable
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
 - GetAnycastIpAddressTable
---

# GetAnycastIpAddressTable function


## -description

The 
<b>GetAnycastIpAddressTable</b> function  retrieves the anycast IP address table on the local computer.

## -parameters

### -param Family [in]

The address family to retrieve. 

Possible values for the address family are listed in the <i>Winsock2.h</i> header file. Note that the values for the AF_ address family and PF_ protocol family constants  are identical (for example, <b>AF_INET</b> and <b>PF_INET</b>), so either constant can be used.

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and possible values for this member are defined in the <i>Ws2def.h</i> header file. Note that the <i>Ws2def.h</i> header file is automatically included in <i>Winsock2.h</i>, and should never be used directly.

The values currently supported are <b>AF_INET</b>, <b>AF_INET6</b>, and <b>AF_UNSPEC</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AF_UNSPEC"></a><a id="af_unspec"></a><dl>
<dt><b>AF_UNSPEC</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The address family is unspecified. When this parameter is specified,  this function  returns the anycast IP address table containing both IPv4 and IPv6 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family. When this parameter is specified,  this function  returns the anycast IP address table containing only  IPv4 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family. When this parameter is specified,  this function  returns the anycast IP address table containing only IPv6 entries. 

</td>
</tr>
</table>

### -param Table [out]

A pointer to a 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_table">MIB_ANYCASTIPADDRESS_TABLE</a> structure that contains a table of anycast IP address entries on the local computer.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the <i>Table</i> parameter or the <i>Family</i> parameter was not specified as <b>AF_INET</b>, <b>AF_INET6</b>, or <b>AF_UNSPEC</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory resources are available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No anycast IP address entries as specified in the <i>Family</i> parameter were found. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported. This error is returned if no IPv4 stack is on the local computer and <b>AF_INET</b> was specified in the <b>Family</b> parameter. This error is also returned if no IPv6 stack is on the local computer and <b>AF_INET6</b> was specified in the <b>Family</b> parameter. This error is also returned on versions of Windows where this function is not supported.

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

The <b>GetAnycastIpAddressTable</b> function is defined on Windows Vista and later. 

The  
<b>GetAnycastIpAddressTable</b> function enumerates the anycast IP addresses on a local system and returns this information in a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_table">MIB_ANYCASTIPADDRESS_TABLE</a> structure. 

The anycast IP address entries are returned in a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_table">MIB_ANYCASTIPADDRESS_TABLE</a> structure in the buffer pointed to by the <i>Table</i> parameter. The <b>MIB_ANYCASTIPADDRESS_TABLE</b> structure contains an anycast IP address entry count and an array of <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_row">MIB_ANYCASTIPADDRESS_ROW</a> structures for each anycast IP address entry. When these returned structures are no longer required, free the memory by calling the <a href="/windows/desktop/api/netioapi/nf-netioapi-freemibtable">FreeMibTable</a>.

The <i>Family</i> parameter must be initialized to either <b>AF_INET</b>,  <b>AF_INET6</b>, or <b>AF_UNSPEC</b>. 

Note that the returned <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_table">MIB_ANYCASTIPADDRESS_TABLE</a> structure pointed to by the <i>Table</i> parameter may contain padding  for alignment between the <b>NumEntries</b> member and the first <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_row">MIB_ANYCASTIPADDRESS_ROW</a> array entry in the <b>Table</b> member of the <b>MIB_ANYCASTIPADDRESS_TABLE</b> structure. Padding for alignment may also be present between the <b>MIB_ANYCASTIPADDRESS_ROW</b> array entries. Any access to a <b>MIB_ANYCASTIPADDRESS_ROW</b> array entry should assume  padding may exist.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-freemibtable">FreeMibTable</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_row">MIB_ANYCASTIPADDRESS_ROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_anycastipaddress_table">MIB_ANYCASTIPADDRESS_TABLE</a>