---
UID: NF:lmshare.NetShareDelEx
title: NetShareDelEx function (lmshare.h)
description: Deletes a share name from a server's list of shared resources, which disconnects all connections to that share.
helpviewer_keywords: ["0","1","2","or 502","503","NetShareDelEx","NetShareDelEx function [Files]","fs.netsharedelex","lmshare/NetShareDelEx"]
old-location: fs\netsharedelex.htm
tech.root: fs
ms.assetid: 2461c533-351b-48f4-b660-cb17ac3398fa
ms.date: 12/05/2018
ms.keywords: 0,1,2,or 502, 503, NetShareDelEx, NetShareDelEx function [Files], fs.netsharedelex, lmshare/NetShareDelEx
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetShareDelEx
 - lmshare/NetShareDelEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetShareDelEx
---

# NetShareDelEx function


## -description

Deletes a share name from a server's list of shared resources, which disconnects all connections to that share. This function, which is an extended version of the <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharedel">NetShareDel</a> function, allows the caller  to specify a <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_0">SHARE_INFO_0</a>, <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a>, <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a>, <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a>, or <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure.

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
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_0">SHARE_INFO_0</a>, <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a>, <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a>, or <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a>  structure.

</td>
</tr>
<tr>
<td width="40%"><a id="503"></a><dl>
<dt><b>503</b></dt>
</dl>
</td>
<td width="60%">
Specifies information about the shared resource, including the name of the resource, type and permissions, number of connections, and other pertinent information. The <i>buf</i> parameter points to a 
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure.

</td>
</tr>
</table>

### -param buf [in]

Pointer to the buffer that specifies the data. The format of this data depends on the value of the <i>level</i> parameter. For more information, see 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a>.

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

If 503 is specified for the <i>level</i> parameter, the <i>buf</i> parameter points to a <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a> structure, and the <b>shi503_netname</b> and <b>shi503_servername</b> members of that structure are used to look up the shared resource on the server; the other members are ignored. The remote server specified in the <b>shi503_servername</b> member must have been bound to a transport protocol using the <a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a> function. In the call to  <b>NetServerTransportAddEx</b>, either 2 or 3 must have been specified for the <i>level</i> parameter, and the <b>SVTI2_SCOPED_NAME</b> flag must have been specified in the <a href="/windows/desktop/api/lmserver/ns-lmserver-server_transport_info_2">SERVER_TRANSPORT_INFO_2</a> structure for the transport protocol.

If 0, 1, 2, or 502 is specified for the <i>level</i> parameter, the <i>buf</i> parameter points to a <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_0">SHARE_INFO_0</a>, <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a>, <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a>, or <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a> structure, and the <b>shi0_netname</b>, <b>shi1_netname</b>, <b>shi2_netname</b>, or <b>shi502_netname</b> member of that structure is used; the other members are ignored.

## -see-also

<a href="/windows/desktop/api/lmserver/nf-lmserver-netservertransportaddex">NetServerTransportAddEx</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netshareadd">NetShareAdd</a>



<a href="/windows/desktop/api/lmshare/nf-lmshare-netsharedel">NetShareDel</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>



<a href="/windows/desktop/NetShare/network-share-functions">Network Share Functions</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_0">SHARE_INFO_0</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1">SHARE_INFO_1</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_2">SHARE_INFO_2</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_502">SHARE_INFO_502</a>



<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_503">SHARE_INFO_503</a>