---
UID: NF:lmserver.NetServerTransportAddEx
title: NetServerTransportAddEx function
author: windows-sdk-content
description: The NetServerTransportAddEx function binds the specified server to the transport protocol.
old-location: netmgmt\netservertransportaddex.htm
old-project: netmgmt
ms.assetid: d1edc75d-8313-422c-a6fb-8b51a309a252
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: 0, 1, 2, 3, NetServerTransportAddEx, NetServerTransportAddEx function [Network Management], _win32_netservertransportaddex, lmserver/NetServerTransportAddEx, netmgmt.netservertransportaddex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmserver.h
req.include-header: Lm.h
req.redist: 
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
tech.root: 
req.typenames: TIME_OF_DAY_INFO, *PTIME_OF_DAY_INFO, *LPTIME_OF_DAY_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetServerTransportAddEx
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetServerTransportAddEx function


## -description


The 
				<b>NetServerTransportAddEx</b> function binds the specified server to the transport protocol. This extended function allows the calling application to specify the 
<a href="https://msdn.microsoft.com/5b94cf7a-74d1-4ae8-87bd-22b2daf292cb">SERVER_TRANSPORT_INFO_0</a>, <a href="https://msdn.microsoft.com/f21fed49-207a-4f64-becd-3d3c1e995eb0">SERVER_TRANSPORT_INFO_1</a>, 
<a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a>, or 
<a href="https://msdn.microsoft.com/045d60d4-518f-4ce4-b611-e23d1588d5d3">SERVER_TRANSPORT_INFO_3</a> information levels.


## -parameters




### -param servername [in]

A pointer to a string that specifies the name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


### -param level [in]

Specifies a value that indicates the information level of the data. This parameter can be one of the following values.

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
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the transport protocol, including name, address, network location, and domain. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/f21fed49-207a-4f64-becd-3d3c1e995eb0">SERVER_TRANSPORT_INFO_1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Specifies the same information as level 1, with the addition of an <b>svti2_flags</b> member. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
 Specifies the same information as level 2, with the addition of credential information. The <i>bufptr</i> parameter points to a 
<a href="https://msdn.microsoft.com/045d60d4-518f-4ce4-b611-e23d1588d5d3">SERVER_TRANSPORT_INFO_3</a> structure.

</td>
</tr>
</table>
 


### -param bufptr [in]

A pointer to the buffer that contains the data. The format of this data depends on the value of the <i>level</i> parameter. 

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

This error is returned if the transport name or transport address member in the <a href="https://msdn.microsoft.com/5b94cf7a-74d1-4ae8-87bd-22b2daf292cb">SERVER_TRANSPORT_INFO_0</a>, <a href="https://msdn.microsoft.com/f21fed49-207a-4f64-becd-3d3c1e995eb0">SERVER_TRANSPORT_INFO_1</a>, 
<a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a>, or 
<a href="https://msdn.microsoft.com/045d60d4-518f-4ce4-b611-e23d1588d5d3">SERVER_TRANSPORT_INFO_3</a> structure pointed to by the <i>bufptr</i> parameter is <b>NULL</b>. This error is also returned if the transport address length member in the <b>SERVER_TRANSPORT_INFO_0</b>, <b>SERVER_TRANSPORT_INFO_1</b>, 
<b>SERVER_TRANSPORT_INFO_2</b>, or 
<b>SERVER_TRANSPORT_INFO_3</b> structure pointed to by the <i>bufptr</i> parameter is zero or larger than MAX_PATH (defined in the <i>Windef.h</i> header file). This error is also returned if the flags member of the <b>SERVER_TRANSPORT_INFO_2</b>, or 
<b>SERVER_TRANSPORT_INFO_3</b> structure pointed to by the <i>bufptr</i> parameter contains an illegal value.

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
<b>NetServerTransportAddEx</b> function.

If you add a transport protocol to a server using a call to the 
<b>NetServerTransportAddEx</b> function, the connection will not remain after the server reboots or restarts.

The 
<a href="https://msdn.microsoft.com/0789fbfe-be91-4849-a31c-1e1a6ae1e70d">NetServerComputerNameAdd</a> function is a utility function. It combines the features of the 
<a href="https://msdn.microsoft.com/db42ac44-d70d-4b89-882a-6ac83fd611fd">NetServerTransportEnum</a> function and the 
<b>NetServerTransportAddEx</b> function, allowing you to specify an emulated server name.

On Windows Server 2008  and Windows Vista with Service Pack 1 (SP1), every name registered with the Windows remote file server (SRV) is designated as either a scoped name or a non-scoped name.  Every share that is added to the system will then either be attached to all of the non-scoped names, or to a single scoped name.  Applications that wish to use the scoping features are responsible for both registering the new name as a scoped endpoint and then creating the shares with an appropriate scope. In this way, legacy uses of the Network Management and Network Share Management functions are not affected in any way since they continue to register shares and names as non-scoped names.  

A scoped endpoint is created by calling the <b>NetServerTransportAddEx</b> function with the <i>level</i> parameter set to 2 and the <i>bufptr</i> parameter pointed to a <a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a> structure with the <b>SVTI2_SCOPED_NAME</b> bit value set in <b>svti2_flags</b> member. A scoped endpoint is also created by calling the <b>NetServerTransportAddEx</b> function with the <i>level</i> parameter set to 3 and the <i>bufptr</i> parameter pointed to a <a href="https://msdn.microsoft.com/045d60d4-518f-4ce4-b611-e23d1588d5d3">SERVER_TRANSPORT_INFO_3</a> structure with the <b>SVTI2_SCOPED_NAME</b> bit value set in <b>svti3_flags</b> member. 

When the <b>SVTI2_SCOPED_NAME</b> bit value is set for a transport, then shares can be added with a corresponding server name (the <b>shi503_servername</b> member of the <a href="fs.share_info_503">SHARE_INFO_503</a> structure) in a scoped fashion using the <a href="https://msdn.microsoft.com/8b51c155-24e8-4d39-b818-eb2d1bb0ee8b">NetShareAdd</a> function.  If there is no transport registered with the <b>SVTI2_SCOPED_NAME</b> bit value and the name provided in <b>shi503_servername</b> member, then the share add in a scoped fashion will not succeed.


The <a href="https://msdn.microsoft.com/8b51c155-24e8-4d39-b818-eb2d1bb0ee8b">NetShareAdd</a> function is used to add a scoped share on a remote server specified in the <i>servername</i> parameter. The remote server specified in the <b>shi503_servername</b> member of the <a href="fs.share_info_503">SHARE_INFO_503</a> passed in the <i>bufptr</i> parameter must have been bound to a transport protocol using the <b>NetServerTransportAddEx</b> function as a scoped endpoint. The <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <b>shi503_servername</b> member of the <a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a> or <a href="https://msdn.microsoft.com/045d60d4-518f-4ce4-b611-e23d1588d5d3">SERVER_TRANSPORT_INFO_3</a> structure for the transport protocol.  The <a href="https://msdn.microsoft.com/2461c533-351b-48f4-b660-cb17ac3398fa">NetShareDelEx</a> function is used to delete a scoped share.  The <a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a> and <a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a> functions are to used to get and set information on a scoped share.  

Scoped endpoints are generally used by the cluster namespace.




## -see-also




<a href="https://msdn.microsoft.com/0789fbfe-be91-4849-a31c-1e1a6ae1e70d">NetServerComputerNameAdd</a>



<a href="https://msdn.microsoft.com/501232ad-2821-4bbd-9f16-0f49984f6101">NetServerComputerNameDel</a>



<a href="https://msdn.microsoft.com/c8521aed-0762-4412-b117-c911fc77049b">NetServerTransportAdd</a>



<a href="https://msdn.microsoft.com/69b22f30-62b1-4dcb-bbb0-aceae8d77f61">NetServerTransportDel</a>



<a href="https://msdn.microsoft.com/db42ac44-d70d-4b89-882a-6ac83fd611fd">NetServerTransportEnum</a>



<a href="https://msdn.microsoft.com/8b51c155-24e8-4d39-b818-eb2d1bb0ee8b">NetShareAdd</a>



<a href="https://msdn.microsoft.com/2461c533-351b-48f4-b660-cb17ac3398fa">NetShareDelEx</a>



<a href="https://msdn.microsoft.com/672ea208-4048-4d2f-9606-ee3e2133765b">NetShareGetInfo</a>



<a href="https://msdn.microsoft.com/216b0b78-87da-4734-ad07-5ad1c9edf494">NetShareSetInfo</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/5b94cf7a-74d1-4ae8-87bd-22b2daf292cb">SERVER_TRANSPORT_INFO_0</a>



<a href="https://msdn.microsoft.com/f21fed49-207a-4f64-becd-3d3c1e995eb0">SERVER_TRANSPORT_INFO_1</a>



<a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a>



<a href="https://msdn.microsoft.com/045d60d4-518f-4ce4-b611-e23d1588d5d3">SERVER_TRANSPORT_INFO_3</a>



<a href="fs.share_info_503">SHARE_INFO_503</a>



<a href="https://msdn.microsoft.com/64342e21-98f1-42d3-b541-46b826391fad">Server and Workstation Transport Functions</a>
 

 

