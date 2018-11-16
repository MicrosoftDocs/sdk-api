---
UID: NF:mprapi.MprAdminAcceptReauthentication
title: MprAdminAcceptReauthentication function
author: windows-sdk-content
description: Remote Access Service calls the MprAdminAcceptReauthentication function whenever the quarantine state of the client changes.
old-location: rras\mpradminacceptreauthentication.htm
tech.root: RRAS
ms.assetid: 58fea0ca-b7c1-4d32-bcfc-10b41e101f30
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MprAdminAcceptReauthentication, MprAdminAcceptReauthentication callback, MprAdminAcceptReauthentication callback function [RAS], mprapi/MprAdminAcceptReauthentication, rras.mpradminacceptreauthentication
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MprAdminAcceptReauthentication
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MprAdminAcceptReauthentication
: 
---

# MprAdminAcceptReauthentication function


## -description


Remote Access Service calls the 
<b>MprAdminAcceptReauthentication</b> function whenever the quarantine state  
of the client changes. <b>MprAdminAcceptReauthentication</b> determines whether the user is allowed to reauthenticate and connect after the quarantine state has changed.

The quarantine state of a connection is determined by the Network Access Protection (NAP) agent, and is stored in the <b>rasQuarState</b> member of the <a href="https://msdn.microsoft.com/f474563e-01c5-4f2a-aec4-477e0ffc7ab2">RAS_CONNECTION_3</a> structure. 


## -parameters




### -param pRasConnection0 [in]

Pointer to a 
<a href="https://msdn.microsoft.com/e2561365-be3f-44cd-bb3c-18b001fc4d5d">RAS_CONNECTION_0</a> structure that describes this connection.


### -param pRasConnection1 [in]

Pointer to a 
<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a> structure that describes this connection.


### -param pRasConnection2 [in]

Pointer to a 
<a href="https://msdn.microsoft.com/5dcc20f0-7447-4256-9dde-18a4a3c95816">RAS_CONNECTION_2</a> structure that describes this connection.


### -param pRasConnection3 [in]

Pointer to a 
 <a href="https://msdn.microsoft.com/f474563e-01c5-4f2a-aec4-477e0ffc7ab2">RAS_CONNECTION_3</a>structure that describes this connection.


## -returns



If 
<b>MprAdminAcceptReauthentication</b> accepts the connection, the return value should be <b>TRUE</b>.

If 
<b>MprAdminAcceptReauthentication</b> rejects the connection, the return value should be <b>FALSE</b>.




## -remarks



Do not call any of the 
<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a> or 
<a href="https://msdn.microsoft.com/e58fa4a6-16d3-4953-bf21-887d08e25af7">RAS User Administration Functions</a> from inside 
<b>MprAdminAcceptReauthentication</b>. Calls to these functions do not return when made from within a callout function.




## -see-also




<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/e2561365-be3f-44cd-bb3c-18b001fc4d5d">RAS_CONNECTION_0</a>



<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a>



<a href="https://msdn.microsoft.com/5dcc20f0-7447-4256-9dde-18a4a3c95816">RAS_CONNECTION_2</a>



<a href="https://msdn.microsoft.com/f474563e-01c5-4f2a-aec4-477e0ffc7ab2">RAS_CONNECTION_3</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

