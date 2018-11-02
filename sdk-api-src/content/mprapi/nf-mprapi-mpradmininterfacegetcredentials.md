---
UID: NF:mprapi.MprAdminInterfaceGetCredentials
title: MprAdminInterfaceGetCredentials function
author: windows-sdk-content
description: Use the MprAdminInterfaceGetCredentials function to retrieve the domain, user name, and password for dialing out on the specified demand-dial interface.
old-location: rras\mpradmininterfacegetcredentials.htm
tech.root: rras
ms.assetid: 0ec18926-1ee9-4e28-9284-9d95d06be2e4
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MprAdminInterfaceGetCredentials, MprAdminInterfaceGetCredentials function [RAS], _mpr_mpradmininterfacegetcredentials, mprapi/MprAdminInterfaceGetCredentials, rras.mpradmininterfacegetcredentials
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminInterfaceGetCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminInterfaceGetCredentials function


## -description


Use the 
<b>MprAdminInterfaceGetCredentials</b> function to retrieve the domain, user name, and password for dialing out on the specified demand-dial interface.


## -parameters




### -param lpwsServer [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the router on which to execute this call. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the call is executed on the local machine.


### -param lpwsInterfaceName [in]

Pointer to a <b>null</b>-terminated Unicode string that specifies the name of the demand-dial interface. Use 
<a href="https://msdn.microsoft.com/a6d353f0-1d68-4a37-89f3-cdab0fc7972a">MprAdminInterfaceGetInfo</a> to obtain the interface name.


### -param lpwsUserName [out]

Pointer to a Unicode string that receives the name of the user. This string should be UNLEN+1 long. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not return the user name.


### -param lpwsPassword [out]

Pointer to a Unicode string that receives the password. This string should be PWLEN+1 long. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not return the password.


### -param lpwsDomainName [out]

Pointer to a Unicode string that receives the domain name. This string should be DNLEN+1 long. 




This parameter is optional. If the calling application specifies <b>NULL</b> for this parameter, the function does not return the domain name.


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
<dt><b>ERROR_CANNOT_FIND_PHONEBOOK_ENTRY</b></dt>
</dl>
</td>
<td width="60%">
The specified interface does not have any demand-dial parameters associated with it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpwsInterfaceName</i> parameter is <b>NULL</b>.
							

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpwsUserName</i>, <i>lpwsPassword</i>, and <i>lpwsDomainName</i> parameters are all <b>NULL</b>.

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
<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -remarks



The <i>lpwsUserName</i>, <i>lpwsPassword</i>, and <i>lpwsDomainName</i> parameters are optional. If the calling application specifies <b>NULL</b> for all three parameters, 
<b>MprAdminInterfaceGetCredentials</b> returns NO_ERROR and the domain, user name, and password are not returned.

The constants UNLEN, PWLEN, and DNLEN are the maximum lengths for the user name, password, and domain name. These constants are defined in lmcons.h.

Note that the order of the parameters in 
<b>MprAdminInterfaceGetCredentials</b> is different from 
<a href="https://msdn.microsoft.com/a5372bfb-185c-4562-afa3-35399c8e2a46">MprAdminInterfaceSetCredentials</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/a5372bfb-185c-4562-afa3-35399c8e2a46">MprAdminInterfaceSetCredentials</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

