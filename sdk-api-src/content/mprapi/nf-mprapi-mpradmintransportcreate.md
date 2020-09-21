---
UID: NF:mprapi.MprAdminTransportCreate
title: MprAdminTransportCreate function (mprapi.h)
description: The MprAdminTransportCreate function loads a new transport, and starts the router manager for the transport.
helpviewer_keywords: ["MprAdminTransportCreate","MprAdminTransportCreate function [RAS]","_mpr_mpradmintransportcreate","mprapi/MprAdminTransportCreate","rras.mpradmintransportcreate"]
old-location: rras\mpradmintransportcreate.htm
tech.root: RRAS
ms.assetid: 14639cec-9c9a-48f5-b7cc-0aaca7ececbc
ms.date: 12/05/2018
ms.keywords: MprAdminTransportCreate, MprAdminTransportCreate function [RAS], _mpr_mpradmintransportcreate, mprapi/MprAdminTransportCreate, rras.mpradmintransportcreate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminTransportCreate
 - mprapi/MprAdminTransportCreate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminTransportCreate
---

# MprAdminTransportCreate function


## -description

The 
<b>MprAdminTransportCreate</b> function loads a new transport, and starts the router manager for the transport.

## -parameters

### -param hMprServer [in]

Handle to the router on which to set the information. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param dwTransportId [in]

A <b>DWORD</b> value that describes the transport configuration type to set. Acceptable values for <i>dwTransportId</i> are listed in the following table.

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

### -param lpwsTransportName [in, optional]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the transport.

### -param pGlobalInfo [in]

Pointer to a buffer that specifies global information for the transport. Use the 
<a href="/windows/desktop/RRAS/router-information-functions">Information Header Functions</a> to manipulate information headers.

### -param dwGlobalInfoSize [in]

Specifies the size, in bytes, of the data pointed to by the <i>pGlobalInfo</i> parameter.

### -param pClientInterfaceInfo [in, optional]

Pointer to a buffer that specifies default client interface information for the transport. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not set the default client interface information.

### -param dwClientInterfaceInfoSize [in, optional]

Specifies the size, in bytes, of the buffer pointed to by the <i>pClientInterfaceInfo</i> parameter.

### -param lpwsDLLPath [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the path to the DLL for the transport.

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
The <i>pGlobalInfo</i> parameter and the <i>pClientInterfaceInfo</i> parameter are both <b>NULL</b>.

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
<dt><b>ERROR_PROTOCOL_ALREADY_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The specified transport is already running on the specified router.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransportId</i> value does not match any supported transport protocol.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmintransportgetinfo">MprAdminTransportGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmintransportsetinfo">MprAdminTransportSetInfo</a>