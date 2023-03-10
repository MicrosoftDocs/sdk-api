---
UID: NF:netioapi.GetInvertedIfStackTable
title: GetInvertedIfStackTable function (netioapi.h)
description: Retrieves a table of inverted network interface stack row entries that specify the relationship of the network interfaces on an interface stack.
helpviewer_keywords: ["GetInvertedIfStackTable","GetInvertedIfStackTable function [IP Helper]","iphlp.getinvertedifstacktable","netioapi/GetInvertedIfStackTable"]
old-location: iphlp\getinvertedifstacktable.htm
tech.root: IpHlp
ms.assetid: d1808ded-2798-46cc-8021-fdbcd3da60ea
ms.date: 12/05/2018
ms.keywords: GetInvertedIfStackTable, GetInvertedIfStackTable function [IP Helper], iphlp.getinvertedifstacktable, netioapi/GetInvertedIfStackTable
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
 - GetInvertedIfStackTable
 - netioapi/GetInvertedIfStackTable
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
 - GetInvertedIfStackTable
---

# GetInvertedIfStackTable function


## -description

The <b>GetInvertedIfStackTable</b> function  retrieves a table of inverted network interface stack row entries that specify the relationship of the network interfaces on an interface stack.

## -parameters

### -param Table [out]

A pointer to a buffer that receives the table of inverted interface stack row entries in a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_table">MIB_INVERTEDIFSTACK_TABLE</a> structure.

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
An invalid parameter was passed to the function. This error is returned if a <b>NULL</b> pointer is passed in the  <i>Table</i> parameter. 

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
No interface stack entries were found.

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
the <a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> function  to obtain the message string for the returned error.

</td>
</tr>
</table>

## -remarks

The <b>GetInvertedIfStackTable</b> function is defined on Windows Vista and later. 

The  
<b>GetInvertedIfStackTable</b> function enumerates the physical and logical network interfaces on an interface stack on a local system and returns this information in an inverted form in the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_table">MIB_INVERTEDIFSTACK_TABLE</a> structure. 

Interface stack entries are returned in a <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_table">MIB_INVERTEDIFSTACK_TABLE</a> structure in the buffer pointed to by the <i>Table</i> parameter. The <b>MIB_INVERTEDIFSTACK_TABLE</b> structure contains an interface stack entry count and an array of <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_row">MIB_INVERTEDIFSTACK_ROW</a> structures for each interface stack entry. 

The relationship between the interfaces in the interface stack is that the interface with index in the <b>HigherLayerInterfaceIndex</b> member of the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_row">MIB_INVERTEDIFSTACK_ROW</a> structure is immediately above the interface with index in the <b>LowerLayerInterfaceIndex</b> member of the <b>MIB_INVERTEDIFSTACK_ROW</b> structure.

Memory is allocated by the <b>GetInvertedIfStackTable</b> function for the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_table">MIB_INVERTEDIFSTACK_TABLE</a> structure and the <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_row">MIB_INVERTEDIFSTACK_ROW</a> entries in this structure. When these returned structures are no longer required, free the memory by calling the <a href="/windows/desktop/api/netioapi/nf-netioapi-freemibtable">FreeMibTable</a>.

Note that the returned <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_table">MIB_INVERTEDIFSTACK_TABLE</a> structure pointed to by the <i>Table</i> parameter may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_row">MIB_INVERTEDIFSTACK_ROW</a> array entry in the <b>Table</b> member of the <b>MIB_INVERTEDIFSTACK_TABLE</b> structure. Padding for alignment may also be present between the <b>MIB_INVERTEDIFSTACK_ROW</b> array entries. Any access to a <b>MIB_INVERTEDIFSTACK_ROW</b> array entry should assume  padding may exist.

## -see-also

<a href="/windows/desktop/api/netioapi/nf-netioapi-freemibtable">FreeMibTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getifentry2">GetIfEntry2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getifstacktable">GetIfStackTable</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getiftable2">GetIfTable2</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-getipinterfaceentry">GetIpInterfaceEntry</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-initializeipinterfaceentry">InitializeIpInterfaceEntry</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ifstack_row">MIB_IFSTACK_ROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ifstack_table">MIB_IFSTACK_TABLE</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2">MIB_IF_ROW2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_if_table2">MIB_IF_TABLE2</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_row">MIB_INVERTEDIFSTACK_ROW</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_invertedifstack_table">MIB_INVERTEDIFSTACK_TABLE</a>



<a href="/windows/desktop/api/netioapi/ns-netioapi-mib_ipinterface_row">MIB_IPINTERFACE_ROW</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-notifyipinterfacechange">NotifyIpInterfaceChange</a>



<a href="/windows/desktop/api/netioapi/nf-netioapi-setipinterfaceentry">SetIpInterfaceEntry</a>