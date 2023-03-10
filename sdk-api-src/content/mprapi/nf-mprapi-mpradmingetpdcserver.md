---
UID: NF:mprapi.MprAdminGetPDCServer
title: MprAdminGetPDCServer function (mprapi.h)
description: The MprAdminGetPDCServer function retrieves the name of the server with the master User Accounts Subsystem (UAS) from either a domain name or a server name. Either the domain name parameter or the server name parameter may be NULL, but not both.
helpviewer_keywords: ["MprAdminGetPDCServer","MprAdminGetPDCServer function [RAS]","_mpr_mpradmingetpdcserver","mprapi/MprAdminGetPDCServer","rras.mpradmingetpdcserver"]
old-location: rras\mpradmingetpdcserver.htm
tech.root: RRAS
ms.assetid: 96bd5e88-5b13-41b2-ab3a-f9995cae36f8
ms.date: 12/05/2018
ms.keywords: MprAdminGetPDCServer, MprAdminGetPDCServer function [RAS], _mpr_mpradmingetpdcserver, mprapi/MprAdminGetPDCServer, rras.mpradmingetpdcserver
req.header: mprapi.h
req.include-header: 
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MprAdminGetPDCServer
 - mprapi/MprAdminGetPDCServer
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
 - MprAdminGetPDCServer
---

# MprAdminGetPDCServer function


## -description

The 
<b>MprAdminGetPDCServer</b> function retrieves the name of the server with the master User Accounts Subsystem (UAS) from either a domain name or a server name. Either the domain name parameter or the server name parameter may be <b>NULL</b>, but not both.

## -parameters

### -param lpszDomain [in]

Pointer to a null-terminated Unicode string that specifies the name of the domain to which the RAS server belongs. This parameter can be <b>NULL</b> if you are running your RAS administration application on a Windows NT/Windows 2000 server that is not participating in a domain. If this parameter is <b>NULL</b>, the <i>lpwsServerName</i> parameter must not be <b>NULL</b>.

### -param lpszServer [in]

Pointer to a null-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server. Specify the name with leading "\\" characters, in the form: <b>\\servername</b>. This parameter can be <b>NULL</b> if the <i>lpwsDomain</i> parameter is not <b>NULL</b>.

### -param lpszPDCServer [out]

Pointer to a buffer that receives a null-terminated Unicode string that contains the name of a domain controller that has the user account database. The buffer should be big enough to hold the server name (UNCLEN +1). The function prefixes the returned server name with leading "\\" characters, in the form: <b>\\servername</b>.

## -returns

If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails the return value is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
The domain specified is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NERR_InvalidComputer</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpwsDomainName</i> parameter is <b>NULL</b>, and <i>lpwsServerName</i> parameter is not valid.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

The 
<b>MprAdminGetPDCServer</b> function can obtain the name of the server with the user accounts database given the name of the RAS server, or the name of the domain in which the RAS server resides. To get the server name, call the 
<a href="/windows/desktop/api/winbase/nf-winbase-getcomputernamea">GetComputerName</a> function

If the server name specified by <i>lpszServer</i> is part of a domain, The server returned by 
<b>MprAdminGetPDCServer</b> will be either the primary domain controller or a backup domain controller.

If the server name specified by <i>lpszServer</i> is a stand-alone Windows NT/Windows 2000 server (that is, the server or workstation does not participate in a domain), then the server name itself is returned in the <i>lpszUserAccountServer</i> buffer.

You can then use the name of the user account server in a call to the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netquerydisplayinformation">NetQueryDisplayInformation</a> function to enumerate the users in the user account database. You can also use the server name in calls to the 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminusergetinfo">MprAdminUserGetInfo</a> and 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminusersetinfo">MprAdminUserSetInfo</a> functions to get and set RAS privileges for a specified user account.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-getcomputernamea">GetComputerName</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminusergetinfo">MprAdminUserGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminusersetinfo">MprAdminUserSetInfo</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netquerydisplayinformation">NetQueryDisplayInformation</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>