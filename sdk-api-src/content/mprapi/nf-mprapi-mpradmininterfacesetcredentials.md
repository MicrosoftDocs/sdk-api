---
UID: NF:mprapi.MprAdminInterfaceSetCredentials
title: MprAdminInterfaceSetCredentials function (mprapi.h)
description: Use MprAdminInterfaceSetCredentials function to set the domain, user name, and password that will be used for dialing out on the specified demand-dial interface.
helpviewer_keywords: ["MprAdminInterfaceSetCredentials","MprAdminInterfaceSetCredentials function [RAS]","_mpr_mpradmininterfacesetcredentials","mprapi/MprAdminInterfaceSetCredentials","rras.mpradmininterfacesetcredentials"]
old-location: rras\mpradmininterfacesetcredentials.htm
tech.root: RRAS
ms.assetid: a5372bfb-185c-4562-afa3-35399c8e2a46
ms.date: 12/05/2018
ms.keywords: MprAdminInterfaceSetCredentials, MprAdminInterfaceSetCredentials function [RAS], _mpr_mpradmininterfacesetcredentials, mprapi/MprAdminInterfaceSetCredentials, rras.mpradmininterfacesetcredentials
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
 - MprAdminInterfaceSetCredentials
 - mprapi/MprAdminInterfaceSetCredentials
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
 - MprAdminInterfaceSetCredentials
---

# MprAdminInterfaceSetCredentials function


## -description

Use 
<b>MprAdminInterfaceSetCredentials</b> function to set the domain, user name, and password that will be used for dialing out on the specified demand-dial interface.

## -parameters

### -param lpwsServer [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the router on which to execute this call. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the call is executed on the local machine.

### -param lpwsInterfaceName [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the demand-dial interface. Use 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a> to obtain the interface name.

### -param lpwsUserName [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the user name. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not change the user name associated with this interface.

### -param lpwsDomainName [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the domain name. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not change the domain name associated with this interface.

### -param lpwsPassword [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the password. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not change the password associated with this interface.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true: 




<ul>
<li>The <i>lpwsInterfaceName</i> parameter is <b>NULL</b>, or it is longer than MAX_INTERFACE_NAME_LEN.</li>
<li>At least one of the <i>lpwsUserName</i>, <i>lpwsPassword</i>, and <i>lpwsDomainName</i> parameters is too long, and therefore invalid. See the Remarks section for more information.</li>
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
Insufficient memory to create a new data structure to contain the credentials.

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
 


<div> </div>

## -remarks

The <i>lpwsUserName</i>, <i>lpwsPassword</i>, and <i>lpwsDomainName</i> parameters are optional. If the calling application specifies <b>NULL</b> for all three parameters, 
<b>MprAdminInterfaceSetCredentials</b> removes all credential information for this interface.

The constants UNLEN, PWLEN, and DNLEN are the maximum lengths for the user name, password, and domain name. These constants are defined in Lmcons.h.

Note that the order of the parameters in 
<b>MprAdminInterfaceSetCredentials</b> is different from 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetcredentials">MprAdminInterfaceGetCredentials</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-formatmessage">FormatMessage</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetcredentials">MprAdminInterfaceGetCredentials</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmininterfacegetinfo">MprAdminInterfaceGetInfo</a>



<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>