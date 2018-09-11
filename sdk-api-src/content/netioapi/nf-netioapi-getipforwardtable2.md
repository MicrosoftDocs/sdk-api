---
UID: NF:netioapi.GetIpForwardTable2
title: GetIpForwardTable2 function
author: windows-sdk-content
description: The GetIpForwardTable2 function retrieves the IP route entries on the local computer.
old-location: iphlp\getipforwardtable2.htm
tech.root: iphlp
ms.assetid: 14412ef1-d970-419d-abfa-389f6ceb638d
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: AF_INET, AF_INET6, AF_UNSPEC, GetIpForwardTable2, GetIpForwardTable2 function [IP Helper], iphlp.getipforwardtable2, netioapi/GetIpForwardTable2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Iphlpapi.dll
api_name:
 - GetIpForwardTable2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetIpForwardTable2 function


## -description


The 
<b>GetIpForwardTable2</b> function retrieves the IP route entries on the local computer.


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
The address family is unspecified. When this parameter is specified,  this function  returns the IP routing table containing both IPv4 and IPv6 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET"></a><a id="af_inet"></a><dl>
<dt><b>AF_INET</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 4 (IPv4) address family. When this parameter is specified,  this function  returns the IP routing table containing only  IPv4 entries. 

</td>
</tr>
<tr>
<td width="40%"><a id="AF_INET6"></a><a id="af_inet6"></a><dl>
<dt><b>AF_INET6</b></dt>
<dt>23</dt>
</dl>
</td>
<td width="60%">
The Internet Protocol version 6 (IPv6) address family. When this parameter is specified,  this function  returns the IP routing table containing only IPv6 entries. 

</td>
</tr>
</table>
 


### -param Table [out]

A pointer to a 
<a href="https://msdn.microsoft.com/9ba938e8-3395-4c9d-b1d2-b2c030783c16">MIB_IPFORWARD_TABLE2</a> structure that contains a table of IP route entries on the local computer. 


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
No IP route entries as specified in the <i>Family</i> parameter were found. 

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
<a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.

</td>
</tr>
</table>
 




## -remarks



The <b>GetIpForwardTable2</b> function is defined on Windows Vista and later. 

The  
<b>GetIpForwardTable2</b> function enumerates the IP route entries on a local system and returns this information in a <a href="https://msdn.microsoft.com/9ba938e8-3395-4c9d-b1d2-b2c030783c16">MIB_IPFORWARD_TABLE2</a> structure. 

The IP route entries are returned in a <a href="https://msdn.microsoft.com/9ba938e8-3395-4c9d-b1d2-b2c030783c16">MIB_IPFORWARD_TABLE2</a> structure in the buffer pointed to by the <i>Table</i> parameter. The <b>MIB_IPFORWARD_TABLE2</b> structure contains an IP route entry count and an array of <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> structures for each IP route entry. When these returned structures are no longer required, free the memory by calling the <a href="https://msdn.microsoft.com/31c8cdc4-73c7-4e82-8226-c90320046199">FreeMibTable</a>.

The <i>Family</i> parameter must be initialized to either <b>AF_INET</b>,  <b>AF_INET6</b>, or <b>AF_UNSPEC</b>. 

Note that the returned <a href="https://msdn.microsoft.com/9ba938e8-3395-4c9d-b1d2-b2c030783c16">MIB_IPFORWARD_TABLE2</a> structure pointed to by the <i>Table</i> parameter may contain padding for alignment between the <b>NumEntries</b> member and the first <a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a> array entry in the <b>Table</b> member of the <b>MIB_IPFORWARD_TABLE2</b> structure. Padding for alignment may also be present between the <b>MIB_IPFORWARD_ROW2</b> array entries. Any access to a <b>MIB_IPFORWARD_ROW2</b> array entry should assume  padding may exist. 






## -see-also




<a href="https://msdn.microsoft.com/d2d065d3-daad-4167-8b87-4229199ee76a">CreateIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/68d5a5a5-21cf-4337-8a35-7f847f5e2138">DeleteIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/31c8cdc4-73c7-4e82-8226-c90320046199">FreeMibTable</a>



<a href="https://msdn.microsoft.com/7bc16824-c98f-4cd5-a589-e198b48b637c">GetBestRoute2</a>



<a href="https://msdn.microsoft.com/53d5009a-d205-40ce-88e5-fe37e72b5a50">GetIpForwardEntry2</a>



<a href="https://msdn.microsoft.com/1968c4e5-4b28-4387-a918-3326bc80bb3e">InitializeIpForwardEntry</a>



<a href="https://msdn.microsoft.com/3678315d-b6ab-48c8-8522-a57deb63f8c9">MIB_IPFORWARD_ROW2</a>



<a href="https://msdn.microsoft.com/9ba938e8-3395-4c9d-b1d2-b2c030783c16">MIB_IPFORWARD_TABLE2</a>



<a href="https://msdn.microsoft.com/f104dc0c-b3e0-4f22-ac5f-5dbf967be31b">NotifyRouteChange2</a>



<a href="https://msdn.microsoft.com/e11aab0b-6d6c-4e90-a60a-f7d68c09751b">SetIpForwardEntry2</a>
 

 

