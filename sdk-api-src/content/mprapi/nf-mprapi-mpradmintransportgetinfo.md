---
UID: NF:mprapi.MprAdminTransportGetInfo
title: MprAdminTransportGetInfo function (mprapi.h)
description: The MprAdminTransportGetInfo function retrieves global information, default client interface information, or both, for a specified transport.
helpviewer_keywords: ["MprAdminTransportGetInfo","MprAdminTransportGetInfo function [RAS]","_mpr_mpradmintransportgetinfo","mprapi/MprAdminTransportGetInfo","rras.mpradmintransportgetinfo"]
old-location: rras\mpradmintransportgetinfo.htm
tech.root: RRAS
ms.assetid: 47fbe483-8a1b-4747-9555-931dd63e2db8
ms.date: 12/05/2018
ms.keywords: MprAdminTransportGetInfo, MprAdminTransportGetInfo function [RAS], _mpr_mpradmintransportgetinfo, mprapi/MprAdminTransportGetInfo, rras.mpradmintransportgetinfo
f1_keywords:
- mprapi/MprAdminTransportGetInfo
dev_langs:
- c++
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Mprapi.dll
api_name:
- MprAdminTransportGetInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminTransportGetInfo function


## -description


The 
<b>MprAdminTransportGetInfo</b> function retrieves global information, default client interface information, or both, for a specified transport.


## -parameters




### -param hMprServer [in]

Handle to the router from which information is being retrieved. This handle is obtained from a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.


### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport type to retrieve. Acceptable values for <i>dwTransportId</i> are listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Transport (Protocol Family)</th>
</tr>
<tr>
<td>PID_ATALK</td>
<td>AppleTalk</td>
</tr>
<tr>
<td>PID_IP</td>
<td>Internet Protocol version 4</td>
</tr>
<tr>
<td>PID_IPX</td>
<td>Internet Packet Exchange</td>
</tr>
<tr>
<td>PID_NBF</td>
<td>NetBIOS Frames Protocol</td>
</tr>
<tr>
<td>PID_IPV6</td>
<td>Windows Server 2008 or later: Internet Protocol version 6</td>
</tr>
</table>
 


### -param ppGlobalInfo [out, optional]

Pointer to a pointer variable. This variable points to an information header that receives global information for this transport. Use the 
<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers. 




Free this memory by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not retrieve the global information.


### -param lpdwGlobalInfoSize [out, optional]

Pointer to a <b>DWORD</b> variable. This variable receives the size, in bytes, of the global information for the transport.


### -param ppClientInterfaceInfo [out, optional]

Pointer to a pointer variable. This variable points to default client interface information for this transport. Free this memory by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not retrieve the client interface information.


### -param lpdwClientInterfaceInfoSize [out, optional]

Pointer to a <b>DWORD</b> variable. This variable receives the size, in bytes, of the client interface information.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling application does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true: 




<ul>
<li>The <i>ppGlobalInfo</i> parameter and the <i>ppClientInterfaceInfo</i> parameter are both <b>NULL</b>.</li>
<li>The <i>ppGlobalInfo</i> parameter does not point to valid memory.</li>
<li>The <i>ppClientInterfaceInfo</i> parameter does not point to valid memory.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransportId</i> value does not match any installed transport.

</td>
</tr>
</table>
 




## -remarks



The <i>ppGlobalInfo</i> and <i>ppClientInterfaceInfo</i> parameters cannot both be <b>NULL</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradmintransportsetinfo">MprAdminTransportSetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>
 

 

