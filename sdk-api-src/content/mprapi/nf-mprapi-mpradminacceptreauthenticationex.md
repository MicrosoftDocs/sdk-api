---
UID: NF:mprapi.MprAdminAcceptReauthenticationEx
title: MprAdminAcceptReauthenticationEx function
author: windows-sdk-content
description: Remote Access Service (RAS) calls the MprAdminAcceptReauthenticationEx function whenever the quarantine state of the client changes.
old-location: rras\mpradminacceptreauthenticationex.htm
old-project: RRAS
ms.assetid: 32ea0cb5-f67d-4dcc-b5d0-705b6847b163
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: MprAdminAcceptReauthenticationEx, MprAdminAcceptReauthenticationEx callback, MprAdminAcceptReauthenticationEx callback function [RAS], mprapi/MprAdminAcceptReauthenticationEx, rras.mpradminacceptreauthenticationex
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Mprapi.h
api_name:
-	MprAdminAcceptReauthenticationEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MprAdminAcceptReauthenticationEx function


## -description


Remote Access Service (RAS) calls the 
<b>MprAdminAcceptReauthenticationEx</b> function whenever the quarantine state  
of the client changes. <b>MprAdminAcceptReauthenticationEx</b> determines whether the user is allowed to reauthenticate and connect after the quarantine state has changed.


## -parameters




### -param pRasConn [in]

A pointer to a 
<a href="https://msdn.microsoft.com/48526073-caeb-463e-b85b-1ef46ca1e2b4">RAS_CONNECTION_EX</a> structure that describes this connection.


## -returns



If 
<b>MprAdminAcceptReauthenticationEx</b> accepts the connection, the return value should be <b>TRUE</b>.

If 
<b>MprAdminAcceptReauthenticationEx</b> rejects the connection, the return value should be <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/58fea0ca-b7c1-4d32-bcfc-10b41e101f30">MprAdminAcceptReauthentication</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

