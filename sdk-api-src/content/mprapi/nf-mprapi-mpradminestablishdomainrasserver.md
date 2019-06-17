---
UID: NF:mprapi.MprAdminEstablishDomainRasServer
title: MprAdminEstablishDomainRasServer function (mprapi.h)
author: windows-sdk-content
description: The MprAdminEstablishDomainRasServer function establishes the given machine as a Remote Access Server in the domain. This function must be executed only on a machine joined to a domain.
old-location: rras\mpradminestablishdomainrasserver.htm
tech.root: RRAS
ms.assetid: 756e267b-73bf-46d3-a1af-d2442ceb7b52
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MprAdminEstablishDomainRasServer, MprAdminEstablishDomainRasServer function [RAS], mprapi/MprAdminEstablishDomainRasServer, rras.mpradminestablishdomainrasserver
ms.topic: function
f1_keywords: ["mprapi/MprAdminEstablishDomainRasServer"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminEstablishDomainRasServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminEstablishDomainRasServer function


## -description


The 
<a href="https://docs.microsoft.com/windows/desktop/api/mprapi/nf-mprapi-mpradminserversetinfo">MprAdminEstablishDomainRasServer</a> function establishes the given machine as a Remote Access  Server in the domain. This function must be executed only on a machine joined to a domain.


## -parameters




### -param pszDomain [in]

The domain  in which you want the server to be advertised. 


### -param pszMachine [in]

The name of the RAS server.


### -param bEnable [in]

A <b>BOOL</b> that is <b>TRUE</b> if the RAS server should be advertised in the domain. Otherwise, it is <b>FALSE</b>.


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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-administration-functions">Router Administration Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>
 

 

