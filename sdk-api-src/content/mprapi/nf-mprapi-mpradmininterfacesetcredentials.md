---
UID: NF:mprapi.MprAdminInterfaceSetCredentials
title: MprAdminInterfaceSetCredentials function
author: windows-sdk-content
description: Use MprAdminInterfaceSetCredentials function to set the domain, user name, and password that will be used for dialing out on the specified demand-dial interface.
old-location: rras\mpradmininterfacesetcredentials.htm
tech.root: rras
ms.assetid: a5372bfb-185c-4562-afa3-35399c8e2a46
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: MprAdminInterfaceSetCredentials, MprAdminInterfaceSetCredentials function [RAS], _mpr_mpradmininterfacesetcredentials, mprapi/MprAdminInterfaceSetCredentials, rras.mpradmininterfacesetcredentials
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
 - MprAdminInterfaceSetCredentials
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/a6d353f0-1d68-4a37-89f3-cdab0fc7972a">MprAdminInterfaceGetInfo</a> to obtain the interface name.


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
<a href="_win32_formatmessage">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

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
<a href="https://msdn.microsoft.com/0ec18926-1ee9-4e28-9284-9d95d06be2e4">MprAdminInterfaceGetCredentials</a>.




## -see-also




<a href="_win32_formatmessage">FormatMessage</a>



<a href="https://msdn.microsoft.com/0ec18926-1ee9-4e28-9284-9d95d06be2e4">MprAdminInterfaceGetCredentials</a>



<a href="https://msdn.microsoft.com/a6d353f0-1d68-4a37-89f3-cdab0fc7972a">MprAdminInterfaceGetInfo</a>



<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

