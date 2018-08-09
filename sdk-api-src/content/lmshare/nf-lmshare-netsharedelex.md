---
UID: NF:lmshare.NetShareDelEx
title: NetShareDelEx function
author: windows-sdk-content
description: Deletes a share name from a server's list of shared resources, which disconnects all connections to that share.
old-location: fs\netsharedelex.htm
old-project: netshare
ms.assetid: 2461c533-351b-48f4-b660-cb17ac3398fa
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 0,1,2,or 502, 503, NetShareDelEx, NetShareDelEx function [Files], fs.netsharedelex, lmshare/NetShareDelEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmshare.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SERVER_TRANSPORT_INFO_3, *PSERVER_TRANSPORT_INFO_3, *LPSERVER_TRANSPORT_INFO_3
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetShareDelEx
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetShareDelEx function


## -description


Deletes a share name from a server's list of shared resources, which disconnects all connections to that share. This function, which is an extended version of the <a href="https://msdn.microsoft.com/374b8f81-b3d6-4967-bd4a-ffd3fdc3cf7c">NetShareDel</a> function, allows the caller  to specify a <a href="https://msdn.microsoft.com/47a74c71-1fcb-4c49-93b5-ea7cf3a0e567">SHARE_INFO_0</a>, <a href="https://msdn.microsoft.com/9bc69340-4ea5-4180-ae5c-667c0a245b66">SHARE_INFO_1</a>, <a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a>, <a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a>, or <a href="https://msdn.microsoft.com/en-us/library/Cc462916(v=VS.85).aspx">SHARE_INFO_503</a> structure.


## -parameters




### -param servername [in]

Pointer to a string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used. 




This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> is defined.


### -param level [in]

Specifies the information level of the data. This parameter can be one of the following values.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0__1__2__or_502"></a><a id="0__1__2__OR_502"></a><dl>
<dt><b>0, 1, 2, or 502</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name of the resource, type and permissions, and number of connections. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/47a74c71-1fcb-4c49-93b5-ea7cf3a0e567">SHARE_INFO_0</a>, <a href="https://msdn.microsoft.com/9bc69340-4ea5-4180-ae5c-667c0a245b66">SHARE_INFO_1</a>, <a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a>, or <a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a>  structure.

</td>
</tr>
<tr>
<td width="40%"><a id="503"></a><dl>
<dt><b>503</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name of the resource, type and permissions, number of connections, and other pertinent information. The <i>buf</i> parameter points to a 
<a href="https://msdn.microsoft.com/en-us/library/Cc462916(v=VS.85).aspx">SHARE_INFO_503</a> structure.

</td>
</tr>
</table>
 


### -param buf [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
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
<dt><b>ERROR_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An internal error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value specified for the <i>level</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The request is not supported.

</td>
</tr>
</table>
 




## -remarks



If 503 is specified for the <i>level</i> parameter, the <i>buf</i> parameter points to a <a href="https://msdn.microsoft.com/en-us/library/Cc462916(v=VS.85).aspx">SHARE_INFO_503</a> structure, and the <b>shi503_netname</b> and <b>shi503_servername</b> members of that structure are used to look up the shared resource on the server; the other members are ignored. The remote server specified in the <b>shi503_servername</b> member must have been bound to a transport protocol using the <a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a> function. In the call to  <b>NetServerTransportAddEx</b>, either 2 or 3 must have been specified for the <i>level</i> parameter, and the <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <a href="https://msdn.microsoft.com/b422eb71-1f93-432d-8283-81432edfe568">SERVER_TRANSPORT_INFO_2</a> structure for the transport protocol.

If 0, 1, 2, or 502 is specified for the <i>level</i> parameter, the <i>buf</i> parameter points to a <a href="https://msdn.microsoft.com/47a74c71-1fcb-4c49-93b5-ea7cf3a0e567">SHARE_INFO_0</a>, <a href="https://msdn.microsoft.com/9bc69340-4ea5-4180-ae5c-667c0a245b66">SHARE_INFO_1</a>, <a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a>, or <a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a> structure, and the <b>shi0_netname</b>, <b>shi1_netname</b>, <b>shi2_netname</b>, or <b>shi502_netname</b> member of that structure is used; the other members are ignored. 




## -see-also




<a href="https://msdn.microsoft.com/d1edc75d-8313-422c-a6fb-8b51a309a252">NetServerTransportAddEx</a>



<a href="https://msdn.microsoft.com/8b51c155-24e8-4d39-b818-eb2d1bb0ee8b">NetShareAdd</a>



<a href="https://msdn.microsoft.com/374b8f81-b3d6-4967-bd4a-ffd3fdc3cf7c">NetShareDel</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>



<a href="https://msdn.microsoft.com/14886bb0-e597-4728-a64f-bc16e82874da">Network Share Functions</a>



<a href="https://msdn.microsoft.com/47a74c71-1fcb-4c49-93b5-ea7cf3a0e567">SHARE_INFO_0</a>



<a href="https://msdn.microsoft.com/9bc69340-4ea5-4180-ae5c-667c0a245b66">SHARE_INFO_1</a>



<a href="https://msdn.microsoft.com/cd152ccd-cd60-455f-b25c-c4939c65e0ab">SHARE_INFO_2</a>



<a href="https://msdn.microsoft.com/306e6704-2068-42da-bcc4-c0772c719ee8">SHARE_INFO_502</a>



<a href="https://msdn.microsoft.com/en-us/library/Cc462916(v=VS.85).aspx">SHARE_INFO_503</a>
 

 

