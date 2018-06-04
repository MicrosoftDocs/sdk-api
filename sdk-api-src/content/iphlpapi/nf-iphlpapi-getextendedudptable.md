---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetExtendedUdpTable function


## -description


The <b>GetExtendedUdpTable</b> function retrieves a table that contains a list of UDP endpoints available to the application.


## -parameters




### -param pUdpTable [out]

A pointer to the table structure that contains the filtered UDP endpoints available to the application.   For information about how to determine the type of table returned based on specific input parameter combinations, see the Remarks section later in this document.


### -param pdwSize [in, out]

The estimated size of the structure returned in <i>pUdpTable</i>, in bytes. If this value is set too small, <b>ERROR_INSUFFICIENT_BUFFER</b> is returned by this function, and this field will contain the correct size of the structure.


### -param bOrder [in]

A value that specifies whether the UDP endpoint table should be sorted. If this parameter is set to <b>TRUE</b>, the UDP endpoints in the table are sorted in ascending order, starting with the lowest local IP address. If this parameter is set to <b>FALSE</b>, the UDP endpoints in the table appear in the order in which they were retrieved.

The following values are compared as listed when ordering the UDP endpoints: <ol>
<li>Local IP address</li>
<li>Local scope ID (applicable when the <i>ulAf</i> parameter is set to AF_INET6)</li>
<li>Local UDP port</li>
</ol>



### -param ulAf [in]

The version of IP used by the UDP endpoint.

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

The type of the UDP table structure to retrieve.  This parameter can be one of the values from the <a href="https://msdn.microsoft.com/2e7304d1-b89c-46d4-9121-936a1c38cc51">UDP_TABLE_CLASS</a> enumeration. 

On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the <a href="https://msdn.microsoft.com/2e7304d1-b89c-46d4-9121-936a1c38cc51">UDP_TABLE_CLASS</a> enumeration  is defined in the <i>Iprtrmib.h</i> header file, not in the <i>Iphlpapi.h</i> header file.

 The <a href="https://msdn.microsoft.com/2e7304d1-b89c-46d4-9121-936a1c38cc51">UDP_TABLE_CLASS</a> enumeration value is combined with the value of the <i>ulAf</i> parameter to determine the extended UDP information to retrieve. 




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
An invalid parameter was passed to the function. This error is returned if the <i>TableClass</i> parameter contains a value that is not defined in the  <a href="https://msdn.microsoft.com/2e7304d1-b89c-46d4-9121-936a1c38cc51">UDP_TABLE_CLASS</a> enumeration.

</td>
</tr>
</table>
 




## -remarks



The table type returned by this function depends on the specific combination of the <i>ulAf</i> parameter and the <i>TableClass</i> parameter. 

When the <i>ulAf</i> parameter is set to <b>AF_INET</b>, the following table indicates the UDP table type to retrieve in the structure pointed to by the <i>pUdpTable</i> parameter for each possible <i>TableClass</i> value.


<table>
<tr>
<th><i>TableClass</i> value</th>
<th><i>pUdpTable</i> structure</th>
</tr>
<tr>
<td><b>UDP_TABLE_BASIC</b></td>
<td>
<a href="https://msdn.microsoft.com/83608d38-e352-483a-b284-2f9cb444e64f">MIB_UDPTABLE</a>
</td>
</tr>
<tr>
<td><b>UDP_TABLE_OWNER_MODULE</b></td>
<td>
<a href="https://msdn.microsoft.com/909749d7-a6be-4b3a-b432-79a5aa6e3f4c">MIB_UDPTABLE_OWNER_MODULE</a>
</td>
</tr>
<tr>
<td><b>UDP_TABLE_OWNER_PID</b></td>
<td>
<a href="https://msdn.microsoft.com/7c51a1e4-1e07-4fb1-8db3-e48229f12aca">MIB_UDPTABLE_OWNER_PID</a>
</td>
</tr>
</table>
 



 When the <i>ulAf</i> parameter is set to <b>AF_INET6</b>, the following table indicates the TCP table type to retrieve in the structure pointed to by the <i>pUdpTable</i> parameter for each possible <i>TableClass</i> value.


<table>
<tr>
<th><i>TableClass</i> value</th>
<th><i>pUdpTable</i> structure</th>
</tr>
<tr>
<td><b>UDP_TABLE_BASIC</b></td>
<td>
<a href="https://msdn.microsoft.com/49da9a1f-f244-464e-96b2-944a286445d4">MIB_UDP6TABLE</a>
</td>
</tr>
<tr>
<td><b>UDP_TABLE_OWNER_MODULE</b></td>
<td>
<a href="https://msdn.microsoft.com/11bf2d6d-b9bc-4a4d-b7b0-6f7d61eb3756">MIB_UDP6TABLE_OWNER_MODULE</a>
</td>
</tr>
<tr>
<td><b>UDP_TABLE_OWNER_PID</b></td>
<td>
<a href="https://msdn.microsoft.com/6c8d1cb9-209b-47a0-b41c-6b4098a4a81e">MIB_UDP6TABLE_OWNER_PID</a>
</td>
</tr>
</table>
 



The <b>GetExtendedUdpTable</b> function when called with the <i>ulAf</i> parameter set to <b>AF_INET6</b> and the <i>TableClass</i> set to <b>UDP_TABLE_BASIC</b> is only supported on  Windows Vista and later. 

On Windows Server 2003 with Service Pack 1 (SP1) and Windows XP with Service Pack 2 (SP2), the <b>GetExtendedUdpTable</b> function called with the <i>ulAf</i> parameter set to <b>AF_INET6</b> and the <i>TableClass</i> set to <b>UDP_TABLE_BASIC</b> fails and returns <b>ERROR_NOT_SUPPORTED</b>.

On the Windows SDK released for Windows Vista
   and later, the organization of header files has changed. The various <a href="https://msdn.microsoft.com/83608d38-e352-483a-b284-2f9cb444e64f">MIB_UDPTABLE</a>  structures are defined in the <i>Udpmib.h</i> header file, not in the <i>Iprtrmib.h</i> header file. Note that the <i>Udpmib.h</i> header file is automatically included in <i>Iprtrmib.h</i>, which is automatically included in the <i>Iphlpapi.h</i> header file. The  <i>Udpmib.h</i> and <i>Iprtrmib.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/49da9a1f-f244-464e-96b2-944a286445d4">MIB_UDP6TABLE</a>



<a href="https://msdn.microsoft.com/11bf2d6d-b9bc-4a4d-b7b0-6f7d61eb3756">MIB_UDP6TABLE_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/6c8d1cb9-209b-47a0-b41c-6b4098a4a81e">MIB_UDP6TABLE_OWNER_PID</a>



<a href="https://msdn.microsoft.com/83608d38-e352-483a-b284-2f9cb444e64f">MIB_UDPTABLE</a>



<a href="https://msdn.microsoft.com/909749d7-a6be-4b3a-b432-79a5aa6e3f4c">MIB_UDPTABLE_OWNER_MODULE</a>



<a href="https://msdn.microsoft.com/7c51a1e4-1e07-4fb1-8db3-e48229f12aca">MIB_UDPTABLE_OWNER_PID</a>



<a href="https://msdn.microsoft.com/2e7304d1-b89c-46d4-9121-936a1c38cc51">UDP_TABLE_CLASS</a>
 

 

