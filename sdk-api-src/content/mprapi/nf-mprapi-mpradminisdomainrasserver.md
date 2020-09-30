---
UID: NF:mprapi.MprAdminIsDomainRasServer
title: MprAdminIsDomainRasServer function (mprapi.h)
description: The MprAdminIsDomainRasServer function returns information regarding whether the given machine is registered as the remote access server in the domain.
helpviewer_keywords: ["MprAdminIsDomainRasServer","MprAdminIsDomainRasServer function [RAS]","mprapi/MprAdminIsDomainRasServer","rras.mpradminisdomainrasserver"]
old-location: rras\mpradminisdomainrasserver.htm
tech.root: RRAS
ms.assetid: 5d9e09f9-3bb7-4877-b9f7-ce045fb30c8f
ms.date: 12/05/2018
ms.keywords: MprAdminIsDomainRasServer, MprAdminIsDomainRasServer function [RAS], mprapi/MprAdminIsDomainRasServer, rras.mpradminisdomainrasserver
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
 - MprAdminIsDomainRasServer
 - mprapi/MprAdminIsDomainRasServer
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
 - MprAdminIsDomainRasServer
---

# MprAdminIsDomainRasServer function


## -description

The 
<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminIsDomainRasServer</a> function returns information regarding whether the given machine is registered as the remote access server in the domain.

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

The follow example code shows the use of the <a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminIsDomainRasServer</a> and <b>MprAdminEstablishDomainRasServer</b> functions.


```cpp
#include <windows.h>
#include <stdio.h>
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
    dwRes = MprAdminServerConnect(pszMachine, &phMprServer);
    if(dwRes != ERROR_SUCCESS){
        wprintf (L"RRAS is not running on %s.\n", pszMachine);
        return dwRes;
    }
     
    // Close RRAS handle. It's not needed.
    MprAdminServerDisconnect(&phMprServer);
 
    // Check to see if pszMachine is a RAS server for the domain
    dwRes = MprAdminIsDomainRasServer (pszDomain, pszMachine, &bIsRegistered);
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

```

## -see-also

<a href="/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>