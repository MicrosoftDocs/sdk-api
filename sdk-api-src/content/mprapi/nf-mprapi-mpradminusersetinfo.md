---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MprAdminUserSetInfo function


## -description


The 
<b>MprAdminUserSetInfo</b> function sets RAS information for the specified user.


## -parameters




### -param lpszServer

TBD


### -param lpszUser

TBD


### -param dwLevel [in]

This parameter can be zero or one, corresponding to the structure type pointed to by the <i>lpbBuffer</i> parameter.

<b>Windows NT Server 4.0 with SP3 and later:  </b>This parameter must be zero. 





### -param lpbBuffer [in]

Pointer to a 
<a href="https://msdn.microsoft.com/f034c6c2-2dac-40bf-b810-9bf6f3eb3c41">RAS_USER_0</a> or <a href="https://msdn.microsoft.com/4699346e-0ed0-4091-a8d5-8a12cd6bfbcf">RAS_USER_1</a> structure that specifies the new RAS information for the user. 




<b>Windows NT Server 4.0 with SP3 and later:  </b>If the <i>dwLevel</i> parameter specifies zero, <i>lpbBuffer</i> should point to a 
<a href="https://msdn.microsoft.com/f034c6c2-2dac-40bf-b810-9bf6f3eb3c41">RAS_USER_0</a> structure.


#### - lpwsServerName [in]

Pointer to a Unicode string that specifies the name of the server  with the master User Accounts Subsystem (UAS). If the remote access server is part of a domain, the computer with the UAS is either the primary domain controller or the backup domain controller. If the remote access server is not part of a domain, then the server itself  stores the UAS. In either case, call the 
<a href="https://msdn.microsoft.com/96bd5e88-5b13-41b2-ab3a-f9995cae36f8">MprAdminGetPDCServer</a> function to obtain the value for this parameter. 




If the server itself stores the UAS, this parameter can be <b>NULL</b>.


#### - lpwsUserName [in]

Pointer to a Unicode string that specifies the name of the user for which to set RAS information.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the following values.

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
<dt><b>ERROR _INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The value of <i>dwLevel</i> is invalid.

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
<dt><b>ERROR_NO_SUCH_USER</b></dt>
</dl>
</td>
<td width="60%">
The user specified by <i>lpwsUserName</i> does not exist on the server specified by <i>lpwsServerName</i>.

</td>
</tr>
</table>
 




## -remarks



This function is available on Windows NT 4.0 if the RRAS redistributable is installed. However, the version of Mprapi.dll that ships with the RRAS redistributable exports the function as 
<a href="https://msdn.microsoft.com/5b049dfd-ecc8-47e4-82cc-71a875752714">RasAdminUserSetInfo</a> rather than 
<b>MprAdminUserSetInfo</b>. Therefore, when using the RRAS redistributable, use 
<a href="_win32_loadlibrary">LoadLibrary</a> and 
<a href="_win32_getprocaddress">GetProcAddress</a> to access this function.




## -see-also




<a href="https://msdn.microsoft.com/96bd5e88-5b13-41b2-ab3a-f9995cae36f8">MprAdminGetPDCServer</a>



<a href="https://msdn.microsoft.com/d04f6925-ac38-4adf-ac2e-701db5435c90">MprAdminUserGetInfo</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/f034c6c2-2dac-40bf-b810-9bf6f3eb3c41">RAS_USER_0</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

