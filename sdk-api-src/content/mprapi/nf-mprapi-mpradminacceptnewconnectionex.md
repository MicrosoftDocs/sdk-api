---
UID: NF:mprapi.MprAdminAcceptNewConnectionEx
title: MprAdminAcceptNewConnectionEx function
author: windows-sdk-content
description: Remote Access Service (RAS) calls the MprAdminAcceptNewConnectionEx function each time a new user dials in and successfully completes a RAS authentication. MprAdminAcceptNewConnectionEx determines whether the user is allowed to connect.
old-location: rras\mpradminacceptnewconnectionex.htm
tech.root: RRAS
ms.assetid: 398dd922-dd83-402f-b7ad-ce9438f15ca9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: MprAdminAcceptNewConnectionEx, MprAdminAcceptNewConnectionEx callback, MprAdminAcceptNewConnectionEx callback function [RAS], mprapi/MprAdminAcceptNewConnectionEx, rras.mpradminacceptnewconnectionex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mprapi.h
api_name:
 - MprAdminAcceptNewConnectionEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminAcceptNewConnectionEx function


## -description


Remote Access Service (RAS) calls the 
<b>MprAdminAcceptNewConnectionEx</b> function each time a new user dials in and successfully completes a RAS authentication. <b>MprAdminAcceptNewConnectionEx</b> determines whether the user is allowed to connect.


## -parameters




### -param pRasConn [in]

A pointer to a 
<a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a> structure structure that describes this connection.


## -returns



This callback function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/6ca7fe28-53e1-49e0-ab3c-4e8e4343c88c">MprAdminAcceptNewConnection</a>



<a href="https://msdn.microsoft.com/72cdcb3c-c44c-405c-ab4b-93bf9c628acf">MprAdminAcceptNewConnection2</a>



<a href="https://msdn.microsoft.com/c457b972-e326-4c6d-b146-f6ce4e18e3ea">MprAdminAcceptNewConnection3</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

