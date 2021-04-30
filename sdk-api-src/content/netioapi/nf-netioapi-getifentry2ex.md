---
UID: NF:netioapi.GetIfEntry2Ex
title: GetIfEntry2Ex function (netioapi.h)
description: Retrieves the specified level of information for the specified interface on the local computer.
helpviewer_keywords: ["GetIfEntry2Ex","GetIfEntry2Ex function [IP Helper]","MibIfEntryNormal","MibIfEntryNormalWithoutStatistics","iphlp.getifentry2ex","netioapi/GetIfEntry2Ex"]
old-location: iphlp\getifentry2ex.htm
tech.root: IpHlp
ms.assetid: 98C25986-1B38-4878-B578-3D30394F49E4
ms.date: 12/05/2018
ms.keywords: GetIfEntry2Ex, GetIfEntry2Ex function [IP Helper], MibIfEntryNormal, MibIfEntryNormalWithoutStatistics, iphlp.getifentry2ex, netioapi/GetIfEntry2Ex
req.header: netioapi.h
req.include-header: Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - GetIfEntry2Ex
 - netioapi/GetIfEntry2Ex
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
 - GetIfEntry2Ex
---

# GetIfEntry2Ex function


## -description

The 
<b>GetIfEntry2Ex</b> function  retrieves the specified level of information for the specified interface on the local computer.

## -parameters

### -param Level [in]

The level of interface information to retrieve. This parameter can be one of the values from the <b>MIB_IF_ENTRY_LEVEL</b> enumeration type defined in the <i>Netioapi.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MibIfEntryNormal"></a><a id="mibifentrynormal"></a><a id="MIBIFENTRYNORMAL"></a><dl>
<dt><b>MibIfEntryNormal</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The values of statistics and state returned in members of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure pointed to by the <i>Row</i> parameter are returned from the top of the filter stack.

</td>
</tr>
<tr>
<td width="40%"><a id="MibIfEntryNormalWithoutStatistics_"></a><a id="mibifentrynormalwithoutstatistics_"></a><a id="MIBIFENTRYNORMALWITHOUTSTATISTICS_"></a><dl>
<dt><b>MibIfEntryNormalWithoutStatistics </b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The values of state (without statistics) returned in members of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure  pointed to by the <i>Row</i> parameter are returned from the top of the filter stack.

</td>
</tr>
</table>

### -param Row [in, out]

A pointer to a 
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure that, on successful return, receives information for an interface on the local computer. On input, the <b>InterfaceLuid</b> or the <b>InterfaceIndex</b> member of the <b>MIB_IF_ROW2</b> must be set to the interface for which to retrieve information.

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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The system cannot find the file specified. This error is returned if the  network interface LUID or interface index specified by the <b>InterfaceLuid</b> or <b>InterfaceIndex</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> pointed to by the <i>Row</i> parameter was not a value on the local machine.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> parameter is passed in the <i>Row</i> parameter. This error is also returned if the both the <b>InterfaceLuid</b> and <b>InterfaceIndex</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> pointed to by the <i>Row</i> parameter  are unspecified.

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
the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The  
<b>GetIfEntry2Ex</b> function retrieves information for a specified interface on a local system and returns this information in a pointer to a  
<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure. <b>GetIfEntry2Ex</b> is an enhanced version of the <a href="/windows/desktop/api/netioapi/nf-netioapi-getifentry2">GetIfEntry2</a> function that allows selecting the level of interface information to retrieve.

On input, at least one of the following members in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure passed in the <i>Row</i> parameter must be initialized: <b>InterfaceLuid</b> or <b>InterfaceIndex</b>.

The fields are used in the order listed above. So if the <b>InterfaceLuid</b> is specified, then this member is used to determine the interface. If no value was set for the  <b>InterfaceLuid</b> member (the value of this member was set to zero), then the <b>InterfaceIndex</b> member is next used to determine the interface. 

On output, the remaining fields of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a> structure pointed to by the <i>Row</i> parameter are filled in.

Note that the <i>Netioapi.h</i> header file is automatically included in <i>Iphlpapi.h</i> header file, and should never be used directly.

## -see-also

<b>GetIfEntry</b>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getifentry2">GetIfEntry2</a>



<a href="/windows/desktop/api/iphlpapi/nf-iphlpapi-getiftable">GetIfTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2ex">GetIfTable2Ex</a>



<a href="/windows/desktop/IpHlp/ip-helper-function-reference">IP Helper Function Reference</a>



<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_ifrow">MIB_IFROW</a>



<a href="/windows/desktop/api/ifmib/ns-ifmib-mib_iftable">MIB_IFTABLE</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_table2">MIB_IF_TABLE2</a>