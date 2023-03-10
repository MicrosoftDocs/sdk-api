---
UID: NF:mprapi.MprAdminServerGetInfo
title: MprAdminServerGetInfo function (mprapi.h)
description: The MprAdminServerGetInfo function retrieves information about the specified RRAS server.
helpviewer_keywords: ["MprAdminServerGetInfo","MprAdminServerGetInfo function [RAS]","_mpr_mpradminservergetinfo","mprapi/MprAdminServerGetInfo","rras.mpradminservergetinfo"]
old-location: rras\mpradminservergetinfo.htm
tech.root: RRAS
ms.assetid: d15dfb60-1239-4552-985f-d3c98f2981f4
ms.date: 12/05/2018
ms.keywords: MprAdminServerGetInfo, MprAdminServerGetInfo function [RAS], _mpr_mpradminservergetinfo, mprapi/MprAdminServerGetInfo, rras.mpradminservergetinfo
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
 - MprAdminServerGetInfo
 - mprapi/MprAdminServerGetInfo
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
 - MprAdminServerGetInfo
---

# MprAdminServerGetInfo function


## -description

The 
<b>MprAdminServerGetInfo</b> function retrieves information about the specified RRAS server.

## -parameters

### -param hMprServer [in]

Handle to the router to query. Obtain this handle by calling <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0, 1, and 2 as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>Windows 2000 Server or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_0">MPR_SERVER_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>Windows Server 2003 or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a>
</td>
</tr>
<tr>
<td>2</td>
<td>Windows Server 2008 or later: <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a>
</td>
</tr>
</table>

### -param lplpbBuffer [out]

On successful completion, a pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_0">MPR_SERVER_0</a>, 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a>,  
or   <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.
					Free the memory for this buffer using 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

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
The <i>lplpbBuffer</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The <i>hMprServer</i> parameter is <b>NULL</b>. 

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_0">MPR_SERVER_0</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminServerSetInfo</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>