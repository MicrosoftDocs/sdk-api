---
UID: NF:mprapi.MprAdminServerGetCredentials
title: MprAdminServerGetCredentials function (mprapi.h)
description: The MprAdminServerGetCredentials function retrieves the pre-shared key for the specified server.
helpviewer_keywords: ["MprAdminServerGetCredentials","MprAdminServerGetCredentials function [RAS]","_mpr_mpradminservergetcredentials","mprapi/MprAdminServerGetCredentials","rras.mpradminservergetcredentials"]
old-location: rras\mpradminservergetcredentials.htm
tech.root: RRAS
ms.assetid: 76211b14-8f6c-48e4-846f-bd5d3a04285d
ms.date: 12/05/2018
ms.keywords: MprAdminServerGetCredentials, MprAdminServerGetCredentials function [RAS], _mpr_mpradminservergetcredentials, mprapi/MprAdminServerGetCredentials, rras.mpradminservergetcredentials
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
 - MprAdminServerGetCredentials
 - mprapi/MprAdminServerGetCredentials
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
 - MprAdminServerGetCredentials
---

# MprAdminServerGetCredentials function


## -description

The 
<b>MprAdminServerGetCredentials</b> function retrieves the pre-shared key for the specified server.

## -parameters

### -param hMprServer [in]

Handle to a Windows server. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is returned in the <i>lplpbBuffer</i> parameter. Must be zero.

### -param lplpbBuffer [out]

On successful completion, a pointer to an <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a> structure that contains the pre-shared key for the server. Free the memory occupied by this structure with 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminbufferfree">MprAdminBufferFree</a>.

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
The <i>lplpbBuffer</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwLevel</i> parameter is not zero.

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

The server maintains a single pre-shared key for all users.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetcredentials">MprAdminServerSetCredentials</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>