---
UID: NF:iphlpapi.GetTcp6Table2
title: GetTcp6Table2 function
author: windows-sdk-content
description: Retrieves the TCP connection table for IPv6.
old-location: iphlp\gettcp6table2.htm
old-project: iphlp
ms.assetid: 435b9198-b921-407c-9441-31cfe77c03f1
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: GetTcp6Table2, GetTcp6Table2 function [IP Helper], iphlp.gettcp6table2, iphlpapi/GetTcp6Table2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - GetTcp6Table2
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetTcp6Table2 function


## -description


The 
<b>GetTcp6Table2</b> function retrieves the TCP connection table for IPv6.


## -parameters




### -param TcpTable [out]

A pointer to a buffer that receives the TCP connection table for IPv6 as a 
<a href="https://msdn.microsoft.com/3cb8568e-ce31-4ed1-aa9e-abcb826c0cea">MIB_TCP6TABLE2</a> structure.


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
<a href="https://msdn.microsoft.com/435b9198-b921-407c-9441-31cfe77c03f1">GetTcp6Table2</a> is unable to write to the memory pointed to by the <i>SizePointer</i> parameter.

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



The <b>GetTcp6Table2</b> function is defined on Windows Vista and later. 

The <b>GetTcp6Table2</b> function is an enhanced version of the <a href="https://msdn.microsoft.com/77150609-d06d-4492-bbd7-21eecd825bde">GetTcp6Table</a> function that also retrieves information on the TCP offload state of the TCP connection.




## -see-also




<a href="https://msdn.microsoft.com/96356a0e-ae0d-4000-9223-a578cbdeaa8b">GetExtendedTcpTable</a>



<a href="https://msdn.microsoft.com/021679fc-91de-4e3b-956d-bb00b1856f20">GetOwnerModuleFromTcp6Entry</a>



<a href="https://msdn.microsoft.com/77150609-d06d-4492-bbd7-21eecd825bde">GetTcp6Table</a>



<a href="https://msdn.microsoft.com/78cfc69d-eae8-49c1-a460-6527a61f773d">GetTcpStatisticsEx</a>



<a href="https://msdn.microsoft.com/e90c5aa0-3126-489b-af44-bf86cb45a6d1">GetTcpTable</a>



<a href="https://msdn.microsoft.com/b3e9eda5-5e86-4790-8b1b-ca9bae44b502">MIB_TCP6ROW</a>



<a href="https://msdn.microsoft.com/bbec3397-0317-40f7-926f-2ec48cf5386d">MIB_TCP6ROW2</a>



<a href="https://msdn.microsoft.com/24f2041c-0a8c-4f2c-8585-ebbb0cad394f">MIB_TCP6ROW_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/d0c9c783-c095-487e-a007-8a10700f9fea">MIB_TCP6ROW_OWNER_PID</a>



<a href="https://msdn.microsoft.com/62bb8544-0a0a-40b5-92cf-9631c9a9987c">MIB_TCP6TABLE</a>



<a href="https://msdn.microsoft.com/3cb8568e-ce31-4ed1-aa9e-abcb826c0cea">MIB_TCP6TABLE2</a>



<a href="https://msdn.microsoft.com/aa52531c-1d4e-44f9-8638-1528beb491f3">MIB_TCP6TABLE_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/93629d1d-e5f2-4ae8-b585-17e39ae4986d">MIB_TCP6TABLE_OWNER_PID</a>
 

 

