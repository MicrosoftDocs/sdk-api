---
UID: NF:mprapi.MprAdminUserGetInfo
title: MprAdminUserGetInfo function
author: windows-sdk-content
description: The MprAdminUserGetInfo function retrieves all RAS information for a particular user.
old-location: rras\mpradminusergetinfo.htm
tech.root: rras
ms.assetid: d04f6925-ac38-4adf-ac2e-701db5435c90
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: MprAdminUserGetInfo, MprAdminUserGetInfo function [RAS], _mpr_mpradminusergetinfo, mprapi/MprAdminUserGetInfo, rras.mpradminusergetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminUserGetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminUserGetInfo function


## -description


The 
<b>MprAdminUserGetInfo</b> function retrieves all RAS information for a particular user.


## -parameters




### -param lpszServer [in]

Pointer to a Unicode string that specifies the name of the server  with the master User Accounts Subsystem (UAS). If the remote access server is part of a domain, the computer with the UAS is either the primary domain controller or the backup domain controller. If the remote access server is not part of a domain, then the server itself  stores the UAS. In either case, call the 
<a href="https://msdn.microsoft.com/96bd5e88-5b13-41b2-ab3a-f9995cae36f8">MprAdminGetPDCServer</a> function to obtain the value for this parameter. 




If the server itself stores the UAS, this parameter can be <b>NULL</b>.


### -param lpszUser [in]

Pointer to a Unicode string that specifies the name of the user for which to get RAS information.


### -param dwLevel [in]

This parameter may be zero or one.

<b>Windows NT Server 4.0 with SP3 and later:  </b>This parameter must be zero. 





### -param lpbBuffer [out]

Pointer to a 
<a href="https://msdn.microsoft.com/f034c6c2-2dac-40bf-b810-9bf6f3eb3c41">RAS_USER_0</a> or <a href="https://msdn.microsoft.com/4699346e-0ed0-4091-a8d5-8a12cd6bfbcf">RAS_USER_1</a> structure. The caller must allocate (and free) the memory for this structure. Upon successful return, this structure contains the RAS data for the specified user. 




<b>Windows NT Server 4.0 with SP3 and later:  </b>If the <i>dwLevel</i> parameter specifies zero, <i>lpbBuffer</i> should point to a 
<a href="https://msdn.microsoft.com/f034c6c2-2dac-40bf-b810-9bf6f3eb3c41">RAS_USER_0</a> structure.


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
<a href="https://msdn.microsoft.com/178ff775-9cd2-43f0-9a9a-dbae337c5fe8">RasAdminUserGetInfo</a> rather than 
<b>MprAdminUserGetInfo</b>. Therefore, when using the RRAS redistributable, use 
<a href="https://msdn.microsoft.com/en-us/library/ms684175(v=VS.85).aspx">LoadLibrary</a> and 
<a href="https://msdn.microsoft.com/en-us/library/ms683212(v=VS.85).aspx">GetProcAddress</a> to access this function.




## -see-also




<a href="https://msdn.microsoft.com/96bd5e88-5b13-41b2-ab3a-f9995cae36f8">MprAdminGetPDCServer</a>



<a href="https://msdn.microsoft.com/7f4d5213-56b4-43d2-93c8-ee5ca50b2a19">MprAdminUserSetInfo</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/f034c6c2-2dac-40bf-b810-9bf6f3eb3c41">RAS_USER_0</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

