---
UID: NF:lmserver.NetServerTransportAdd
title: NetServerTransportAdd function (lmserver.h)
author: windows-sdk-content
description: The NetServerTransportAdd function binds the server to the transport protocol.
old-location: netmgmt\netservertransportadd.htm
tech.root: NetMgmt
ms.assetid: c8521aed-0762-4412-b117-c911fc77049b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0, NetServerTransportAdd, NetServerTransportAdd function [Network Management], _win32_netservertransportadd, lmserver/NetServerTransportAdd, netmgmt.netservertransportadd
ms.topic: function
req.header: lmserver.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetServerTransportAdd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NetServerTransportAdd function


## -description


The 
				<b>NetServerTransportAdd</b> function binds the server to the transport protocol.

The extended function 
<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a> allows the calling application to specify the 
<a href="https://msdn.microsoft.com/f21fed49-207a-4f64-becd-3d3c1e995eb0">SERVER_TRANSPORT_INFO_1</a>, 
<a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a>, and 
<a href="https://msdn.microsoft.com/045d60d4-518f-4ce4-b611-e23d1588d5d3">SERVER_TRANSPORT_INFO_3</a> information levels.


## -parameters




### -param servername [in]

A pointer to a string that specifies the name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 





### -param level [in]

Specifies the information level of the data. This parameter can be the following value. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the transport protocol, including name, address, and location on the network. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/5b94cf7a-74d1-4ae8-87bd-22b2daf292cb">SERVER_TRANSPORT_INFO_0</a> structure.

</td>
</tr>
</table>
 


### -param bufptr [in]

A pointer to the buffer that contains the data.

For more information, see 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DUP_NAME</b></dt>
</dl>
</td>
<td width="60%">
A duplicate name exists on the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DOMAINNAME</b></dt>
</dl>
</td>
<td width="60%">
The domain name could not be found on the network.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid. 

This error is returned if the <b>svti0_transportname</b> or <b>svti0_transportaddress</b> member in the <a href="https://msdn.microsoft.com/5b94cf7a-74d1-4ae8-87bd-22b2daf292cb">SERVER_TRANSPORT_INFO_0</a> structure pointed to by the <i>bufptr</i> parameter is <b>NULL</b>. This error is also returned if the <b>svti0_transportaddresslength</b> member in the <b>SERVER_TRANSPORT_INFO_0</b> structure pointed to by the <i>bufptr</i> parameter is zero or larger than MAX_PATH (defined in the Windef.h header file). 

This error is also returned for other invalid parameters.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available.

</td>
</tr>
</table>
 




## -remarks



Only members of the Administrators or Server Operators local group can successfully execute the 
<b>NetServerTransportAdd</b> function.

If you add a transport protocol to a server using a call to the 
<b>NetServerTransportAdd</b> function, the connection will not remain after the server reboots or restarts.




## -see-also




<a href="https://msdn.microsoft.com/0789fbfe-be91-4849-a31c-1e1a6ae1e70d">NetServerComputerNameAdd</a>



<a href="https://msdn.microsoft.com/501232ad-2821-4bbd-9f16-0f49984f6101">NetServerComputerNameDel</a>



<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a>



<a href="https://msdn.microsoft.com/69b22f30-62b1-4dcb-bbb0-aceae8d77f61">NetServerTransportDel</a>



<a href="https://msdn.microsoft.com/db42ac44-d70d-4b89-882a-6ac83fd611fd">NetServerTransportEnum</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/5b94cf7a-74d1-4ae8-87bd-22b2daf292cb">SERVER_TRANSPORT_INFO_0</a>



<a href="https://msdn.microsoft.com/f21fed49-207a-4f64-becd-3d3c1e995eb0">SERVER_TRANSPORT_INFO_1</a>



<a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a>



<a href="https://msdn.microsoft.com/045d60d4-518f-4ce4-b611-e23d1588d5d3">SERVER_TRANSPORT_INFO_3</a>



<a href="https://msdn.microsoft.com/64342e21-98f1-42d3-b541-46b826391fad">Server and Workstation Transport Functions</a>
 

 

