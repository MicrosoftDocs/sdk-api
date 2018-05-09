---
UID: NF:mprapi.MprAdminGetPDCServer
title: MprAdminGetPDCServer function
author: windows-driver-content
description: The MprAdminGetPDCServer function retrieves the name of the server with the master User Accounts Subsystem (UAS) from either a domain name or a server name. Either the domain name parameter or the server name parameter may be NULL, but not both.
old-location: rras\mpradmingetpdcserver.htm
old-project: RRAS
ms.assetid: 96bd5e88-5b13-41b2-ab3a-f9995cae36f8
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: MprAdminGetPDCServer, MprAdminGetPDCServer function [RAS], _mpr_mpradmingetpdcserver, mprapi/MprAdminGetPDCServer, rras.mpradmingetpdcserver
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprAdminGetPDCServer
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminGetPDCServer function


## -description


The 
<b>MprAdminGetPDCServer</b> function retrieves the name of the server with the master User Accounts Subsystem (UAS) from either a domain name or a server name. Either the domain name parameter or the server name parameter may be <b>NULL</b>, but not both.


## -parameters




### -param lpszDomain

TBD


### -param lpszServer

TBD


### -param lpszPDCServer

TBD




#### - lpwsDomainName [in]

Pointer to a null-terminated Unicode string that specifies the name of the domain to which the RAS server belongs. This parameter can be <b>NULL</b> if you are running your RAS administration application on a Windows NT/Windows 2000 server that is not participating in a domain. If this parameter is <b>NULL</b>, the <i>lpwsServerName</i> parameter must not be <b>NULL</b>.


#### - lpwsPDCName [out]

Pointer to a buffer that receives a null-terminated Unicode string that contains the name of a domain controller that has the user account database. The buffer should be big enough to hold the server name (UNCLEN +1). The function prefixes the returned server name with leading "\\" characters, in the form: <b>\\servername</b>.


#### - lpwsServerName [in]

Pointer to a null-terminated Unicode string that specifies the name of the Windows NT/Windows 2000 RAS server. Specify the name with leading "\\" characters, in the form: <b>\\servername</b>. This parameter can be <b>NULL</b> if the <i>lpwsDomain</i> parameter is not <b>NULL</b>.


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
<a href="_win32_getcomputername">GetComputerName</a> function

If the server name specified by <i>lpszServer</i> is part of a domain, The server returned by 
<b>MprAdminGetPDCServer</b> will be either the primary domain controller or a backup domain controller.

If the server name specified by <i>lpszServer</i> is a stand-alone Windows NT/Windows 2000 server (that is, the server or workstation does not participate in a domain), then the server name itself is returned in the <i>lpszUserAccountServer</i> buffer.

You can then use the name of the user account server in a call to the 
<a href="_win32_netquerydisplayinformation">NetQueryDisplayInformation</a> function to enumerate the users in the user account database. You can also use the server name in calls to the 
<a href="https://msdn.microsoft.com/d04f6925-ac38-4adf-ac2e-701db5435c90">MprAdminUserGetInfo</a> and 
<a href="https://msdn.microsoft.com/7f4d5213-56b4-43d2-93c8-ee5ca50b2a19">MprAdminUserSetInfo</a> functions to get and set RAS privileges for a specified user account.




## -see-also




<a href="_win32_getcomputername">GetComputerName</a>



<a href="https://msdn.microsoft.com/d04f6925-ac38-4adf-ac2e-701db5435c90">MprAdminUserGetInfo</a>



<a href="https://msdn.microsoft.com/7f4d5213-56b4-43d2-93c8-ee5ca50b2a19">MprAdminUserSetInfo</a>



<a href="_win32_netquerydisplayinformation">NetQueryDisplayInformation</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

