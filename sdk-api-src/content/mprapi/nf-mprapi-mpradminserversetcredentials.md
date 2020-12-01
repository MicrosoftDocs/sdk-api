---
UID: NF:mprapi.MprAdminServerSetCredentials
title: MprAdminServerSetCredentials function (mprapi.h)
description: The MprAdminServerSetCredentials functions sets the pre-shared key for the specified server.
helpviewer_keywords: ["MprAdminServerSetCredentials","MprAdminServerSetCredentials function [RAS]","_mpr_mpradminserversetcredentials","mprapi/MprAdminServerSetCredentials","rras.mpradminserversetcredentials"]
old-location: rras\mpradminserversetcredentials.htm
tech.root: RRAS
ms.assetid: cc77007f-306f-467a-a52f-bf920da15e74
ms.date: 12/05/2018
ms.keywords: MprAdminServerSetCredentials, MprAdminServerSetCredentials function [RAS], _mpr_mpradminserversetcredentials, mprapi/MprAdminServerSetCredentials, rras.mpradminserversetcredentials
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
 - MprAdminServerSetCredentials
 - mprapi/MprAdminServerSetCredentials
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
 - MprAdminServerSetCredentials
---

# MprAdminServerSetCredentials function


## -description

The 
<b>MprAdminServerSetCredentials</b> functions sets the pre-shared key for the specified server.

## -parameters

### -param hMprServer [in]

Handle to a Windows server. Obtain this handle by calling 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminmibserverconnect">MprAdminMIBServerConnect</a>.

### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lpbBuffer</i> parameter. Must be zero.

### -param lpbBuffer [in]

A pointer to an <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a> structure that contains the pre-shared key for the server.

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
The <i>lpbBuffer</i> parameter is <b>NULL</b>.

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

To delete the pre-shared key, call 
<b>MprAdminServerSetCredentials</b> with the <a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a><b>dwSize</b> member set to zero.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_credentialsex_1">MPR_CREDENTIALSEX_1</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminservergetcredentials">MprAdminServerGetCredentials</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>