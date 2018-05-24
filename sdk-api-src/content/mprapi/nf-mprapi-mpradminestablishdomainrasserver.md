---
UID: NF:mprapi.MprAdminEstablishDomainRasServer
title: MprAdminEstablishDomainRasServer function
author: windows-driver-content
description: The MprAdminEstablishDomainRasServer function establishes the given machine as a Remote Access Server in the domain. This function must be executed only on a machine joined to a domain.
old-location: rras\mpradminestablishdomainrasserver.htm
old-project: RRAS
ms.assetid: 756e267b-73bf-46d3-a1af-d2442ceb7b52
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: MprAdminEstablishDomainRasServer, MprAdminEstablishDomainRasServer function [RAS], mprapi/MprAdminEstablishDomainRasServer, rras.mpradminestablishdomainrasserver
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	MprAdminEstablishDomainRasServer
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminEstablishDomainRasServer function


## -description


The 
<a href="https://msdn.microsoft.com/37187f6f-388e-47d6-83a8-92c2f69f71d9">MprAdminEstablishDomainRasServer</a> function establishes the given machine as a Remote Access  Server in the domain. This function must be executed only on a machine joined to a domain.


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




<a href="https://msdn.microsoft.com/a61734a7-b171-4e38-8dec-46be9a9c08ee">Router Administration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

