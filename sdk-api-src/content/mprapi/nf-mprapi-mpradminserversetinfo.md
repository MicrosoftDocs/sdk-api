---
UID: NF:mprapi.MprAdminServerSetInfo
title: MprAdminServerSetInfo function (mprapi.h)
description: The MprAdminServerSetInfo function is used to set the number of ports for L2TP, PPTP, and SSTP devices when the RRAS service is running.
helpviewer_keywords: ["MprAdminServerSetInfo","MprAdminServerSetInfo function [RAS]","mprapi/MprAdminServerSetInfo","rras.mpradminserversetinfo"]
old-location: rras\mpradminserversetinfo.htm
tech.root: RRAS
ms.assetid: 37187f6f-388e-47d6-83a8-92c2f69f71d9
ms.date: 12/05/2018
ms.keywords: MprAdminServerSetInfo, MprAdminServerSetInfo function [RAS], mprapi/MprAdminServerSetInfo, rras.mpradminserversetinfo
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminServerSetInfo
 - mprapi/MprAdminServerSetInfo
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
 - MprAdminServerSetInfo
---

# MprAdminServerSetInfo function


## -description

The 
<b>MprAdminServerSetInfo</b> function is used to set the number of ports for L2TP, PPTP, and SSTP  devices when the RRAS service is running.

## -parameters

### -param hMprServer [in]

Handle to the router to query. Obtain this handle by calling <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lpbBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 1 and 2 as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
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

### -param lpbBuffer [in]

A pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a>  
or   <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.

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
<dt><b>ERROR_SUCCESS_REBOOT_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
A system reboot is required for such a change to take affect. Change the port count using the <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfo">MprConfigServerSetInfo</a> call and reboot.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
If you try to set the number of ports to more than the system supported limits as defined on the <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a> and <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a> topics.

Returns this error if you try to set the number of PPTP ports to 0.

Returns this error if the flags are not valid or if <i>lpbBuffer</i> or <i>hMprServer</i> is <b>NULL</b>.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DDM_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
RRAS service is not running on this server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>dwLevel</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>hMprServer</i> handle is invalid.

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
<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>

## -remarks

This function is used to set the port count for L2TP, PPTP, and SSTP ports and enable or disable RRAS when the service is running. These values are persistent, meaning that you do not have to follow this call with a call to <a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigserversetinfo">MprConfigServerSetInfo</a>. Note that this function is asynchronous, so you might not see the affect of the changes immediately.


#### Examples

The topic <a href="/windows/desktop/RRAS/setting-l2tp-and-pptp-ports">Setting L2TP and PPTP ports of a local RRAS service</a> shows this function in use.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserverconnect">MprAdminServerConnect</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminservergetinfo">MprAdminServerGetInfo</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>