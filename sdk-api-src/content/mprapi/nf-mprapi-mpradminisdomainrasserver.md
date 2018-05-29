---
UID: NF:mprapi.MprAdminIsDomainRasServer
title: MprAdminIsDomainRasServer function
author: windows-sdk-content
description: The MprAdminIsDomainRasServer function returns information regarding whether the given machine is registered as the remote access server in the domain.
old-location: rras\mpradminisdomainrasserver.htm
old-project: RRAS
ms.assetid: 5d9e09f9-3bb7-4877-b9f7-ce045fb30c8f
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: MprAdminIsDomainRasServer, MprAdminIsDomainRasServer function [RAS], mprapi/MprAdminIsDomainRasServer, rras.mpradminisdomainrasserver
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprAdminIsDomainRasServer
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminIsDomainRasServer function


## -description


The 
<a href="https://msdn.microsoft.com/37187f6f-388e-47d6-83a8-92c2f69f71d9">MprAdminIsDomainRasServer</a> function returns information regarding whether the given machine is registered as the remote access server in the domain. 


## -parameters




### -param pszDomain [in]

The domain  in which you want to query the remote access server.


### -param pszMachine [in]

The name of the remote access server.


### -param pbIsRasServer [out]

Returns <b>TRUE</b> if the machine is registered in the domain, otherwise it returns <b>FALSE</b>.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DS_SERVER_DOWN</b></dt>
</dl>
</td>
<td width="60%">
pszDomain is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
pszMachine is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DS_OPERATIONS_ERROR</b></dt>
</dl>
</td>
<td width="60%">
User is a non-domain user.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SUCH_DOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Function executed on a machine not joined to any domain.

</td>
</tr>
</table>
 




## -remarks



This function must be executed only on a machine joined to a domain.


#### Examples

The follow example code shows the use of the <a href="https://msdn.microsoft.com/37187f6f-388e-47d6-83a8-92c2f69f71d9">MprAdminIsDomainRasServer</a> and <b>MprAdminEstablishDomainRasServer</b> functions.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include "mprapi.h"
#pragma comment(lib, "mprapi.lib")

int __cdecl main(){
    
    // The domain and RAS machine names being queried. These MUST be changed before using this sample code.
    PWCHAR pszDomain = L"YourDomainName.com";
    PWCHAR pszMachine = L"YourRASMachine";
    
    BOOL bIsRegistered = FALSE;
    DWORD dwRes = ERROR_SUCCESS;
    MPR_SERVER_HANDLE phMprServer;

    // Make sure RRAS is running on the remote server
    dwRes = MprAdminServerConnect(pszMachine, &amp;phMprServer);
    if(dwRes != ERROR_SUCCESS){
        wprintf (L"RRAS is not running on %s.\n", pszMachine);
        return dwRes;
    }
     
    // Close RRAS handle. It's not needed.
    MprAdminServerDisconnect(&amp;phMprServer);
 
    // Check to see if pszMachine is a RAS server for the domain
    dwRes = MprAdminIsDomainRasServer (pszDomain, pszMachine, &amp;bIsRegistered);
    if (dwRes != ERROR_SUCCESS){
        //
        // Handle errors here
        //
       return dwRes;
    }

    if (bIsRegistered == TRUE){
        wprintf (L"The RRAS Server on %s is already registered in domain %s.\n", pszMachine, pszDomain);
        return ERROR_SUCCESS;
    }

    wprintf (L"The RRAS Server on %s is NOT registered in domain %s. Registering now...\n", pszMachine, pszDomain);
    dwRes = MprAdminEstablishDomainRasServer (pszDomain, pszMachine, TRUE);
    if (dwRes != ERROR_SUCCESS){
        //
        // Handle errors here
        //
        return dwRes;
    }
    return ERROR_SUCCESS;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

