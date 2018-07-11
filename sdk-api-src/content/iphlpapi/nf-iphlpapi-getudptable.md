---
UID: NF:iphlpapi.GetUdpTable
title: GetUdpTable function
author: windows-sdk-content
description: Retrieves the IPv4 User Datagram Protocol (UDP) listener table.
old-location: iphlp\getudptable.htm
old-project: iphlp
ms.assetid: 00e80e90-1a6d-426d-90cd-20b967ebbb8e
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetUdpTable, GetUdpTable function [IP Helper], _iphlp_getudptable, iphlp.getudptable, iphlpapi/GetUdpTable
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: NET_ADDRESS_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetUdpTable
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetUdpTable function


## -description


The 
<b>GetUdpTable</b> function retrieves the IPv4 User Datagram Protocol (UDP) listener table.


## -parameters




### -param UdpTable

TBD


### -param SizePointer

TBD


### -param Order

TBD




#### - bOrder [in]

A Boolean value that specifies whether the returned UDP listener table should be sorted. If this parameter is <b>TRUE</b>, the table is sorted in the order of: 


<ol>
<li>Local IP address</li>
<li>Local port</li>
</ol>



#### - pUdpTable [out]

A pointer to a buffer that receives the IPv4 UDP listener table as a 
<a href="https://msdn.microsoft.com/83608d38-e352-483a-b284-2f9cb444e64f">MIB_UDPTABLE</a> structure.


#### - pdwSize [in, out]

On input, specifies the size in bytes of the buffer pointed to by the <i>UdpTable</i> parameter. 




On output, if the buffer is not large enough to hold the returned listener table, the function sets this parameter equal to the required buffer size in bytes.

On the Windows SDK released for Windows Vista and later, the data type for this parameter is changed to a <b>PULONG</b> which is equivalent to a <b>PDWORD</b>. 


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
<a href="https://msdn.microsoft.com/00e80e90-1a6d-426d-90cd-20b967ebbb8e">GetUdpTable</a> is unable to write to the memory pointed to by the <i>pdwSize</i> parameter.

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



On the Windows SDK released for Windows Vista and later, the return value from the <b>GetUdpTable</b> function is changed to a data type of <b>ULONG</b> which is equivalent to a <b>DWORD</b>. 




## -see-also




<a href="https://msdn.microsoft.com/c936d5a0-ca5e-487e-b304-bfd81403ab40">GetExtendedUdpTable</a>



<a href="https://msdn.microsoft.com/01ed27b6-3ca6-4c9c-8910-a71a073c2ca2">GetOwnerModuleFromUdp6Entry</a>



<a href="https://msdn.microsoft.com/bd8f82b0-4a2d-48f1-8ae7-85257c6ae656">GetOwnerModuleFromUdpEntry</a>



<a href="https://msdn.microsoft.com/5e86483c-aa39-4d6c-a9b4-9b046b3dcc74">GetUdp6Table</a>



<a href="https://msdn.microsoft.com/a86e5758-a984-4483-8e9c-c482a7676a20">GetUdpStatistics</a>



<a href="https://msdn.microsoft.com/9de7fa95-6bda-4fcc-b563-aed2e61fc1c7">GetUdpStatisticsEx</a>



<a href="https://msdn.microsoft.com/db366802-962f-4e83-838e-1e2f51beab92">MIB_UDPROW</a>



<a href="https://msdn.microsoft.com/9ae304e0-4653-4757-a823-d4ccf68627bf">MIB_UDPROW_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/b914b6eb-adf9-4a61-ae8f-05d3ff90ce90">MIB_UDPROW_OWNER_PID</a>



<a href="https://msdn.microsoft.com/83608d38-e352-483a-b284-2f9cb444e64f">MIB_UDPTABLE</a>



<a href="https://msdn.microsoft.com/909749d7-a6be-4b3a-b432-79a5aa6e3f4c">MIB_UDPTABLE_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/7c51a1e4-1e07-4fb1-8db3-e48229f12aca">MIB_UDPTABLE_OWNER_PID</a>
 

 

