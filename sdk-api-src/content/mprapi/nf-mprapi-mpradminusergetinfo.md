---
UID: NF:mprapi.MprAdminUserGetInfo
title: MprAdminUserGetInfo function (mprapi.h)
description: The MprAdminUserGetInfo function retrieves all RAS information for a particular user.
helpviewer_keywords: ["MprAdminUserGetInfo","MprAdminUserGetInfo function [RAS]","_mpr_mpradminusergetinfo","mprapi/MprAdminUserGetInfo","rras.mpradminusergetinfo"]
old-location: rras\mpradminusergetinfo.htm
tech.root: RRAS
ms.assetid: d04f6925-ac38-4adf-ac2e-701db5435c90
ms.date: 12/05/2018
ms.keywords: MprAdminUserGetInfo, MprAdminUserGetInfo function [RAS], _mpr_mpradminusergetinfo, mprapi/MprAdminUserGetInfo, rras.mpradminusergetinfo
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
 - MprAdminUserGetInfo
 - mprapi/MprAdminUserGetInfo
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
 - MprAdminUserGetInfo
---

# MprAdminUserGetInfo function


## -description

The 
<b>MprAdminUserGetInfo</b> function retrieves all RAS information for a particular user.

## -parameters

### -param lpszServer [in]

Pointer to a Unicode string that specifies the name of the server  with the master User Accounts Subsystem (UAS). If the remote access server is part of a domain, the computer with the UAS is either the primary domain controller or the backup domain controller. If the remote access server is not part of a domain, then the server itself  stores the UAS. In either case, call the 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmingetpdcserver">MprAdminGetPDCServer</a> function to obtain the value for this parameter. 




If the server itself stores the UAS, this parameter can be <b>NULL</b>.

### -param lpszUser [in]

Pointer to a Unicode string that specifies the name of the user for which to get RAS information.

### -param dwLevel [in]

This parameter may be zero or one.

<b>Windows NT Server 4.0 with SP3 and later:  </b>This parameter must be zero.

### -param lpbBuffer [out]

Pointer to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_user_0">RAS_USER_0</a> or <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_user_1">RAS_USER_1</a> structure. The caller must allocate (and free) the memory for this structure. Upon successful return, this structure contains the RAS data for the specified user. 




<b>Windows NT Server 4.0 with SP3 and later:  </b>If the <i>dwLevel</i> parameter specifies zero, <i>lpbBuffer</i> should point to a 
<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_user_0">RAS_USER_0</a> structure.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails the return value is one of the following values.

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
The caller does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>dwLevel</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>lpbBuffer</i> is <b>NULL</b>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_USER</b></dt>
</dl>
</td>
<td width="60%">
The user specified by <i>lpwsUserName</i> does not exist on the server specified by <i>lpwsServerName</i>.

</td>
</tr>
</table>

## -remarks

This function is available on Windows NT 4.0 if the RRAS redistributable is installed. However, the version of Mprapi.dll that ships with the RRAS redistributable exports the function as 
<a href="/windows/desktop/RRAS/rasadminusergetinfo">RasAdminUserGetInfo</a> rather than 
<b>MprAdminUserGetInfo</b>. Therefore, when using the RRAS redistributable, use 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and 
<a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access this function.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradmingetpdcserver">MprAdminGetPDCServer</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminusersetinfo">MprAdminUserSetInfo</a>



<a href="/windows/desktop/RRAS/ras-administration-functions">RAS Administration Functions</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_user_0">RAS_USER_0</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>