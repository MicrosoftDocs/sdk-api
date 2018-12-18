---
UID: NF:mprapi.MprAdminAcceptNewConnection
title: MprAdminAcceptNewConnection function
author: windows-sdk-content
description: Remote Access Service calls the MprAdminAcceptNewConnection function each time a new user dials in and successfully completes RAS authentication. MprAdminAcceptNewConnection determines whether the user is allowed to connect.
old-location: rras\mpradminacceptnewconnection.htm
tech.root: rras
ms.assetid: 6ca7fe28-53e1-49e0-ab3c-4e8e4343c88c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MprAdminAcceptNewConnection, MprAdminAcceptNewConnection callback, MprAdminAcceptNewConnection callback function [RAS], _mpr_mpradminacceptnewconnection, mprapi/MprAdminAcceptNewConnection, rras.mpradminacceptnewconnection
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
 - MprAdminAcceptNewConnection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminAcceptNewConnection function


## -description


Remote Access Service calls the 
<b>MprAdminAcceptNewConnection</b> function each time a new user dials in and successfully completes RAS authentication. 
<b>MprAdminAcceptNewConnection</b> determines whether the user is allowed to connect.


## -parameters




### -param pRasConnection0 [in]

Pointer to a 
<a href="https://msdn.microsoft.com/e2561365-be3f-44cd-bb3c-18b001fc4d5d">RAS_CONNECTION_0</a> structure that describes this connection.


### -param pRasConnection1 [in]

Pointer to a 
<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a> structure that describes this connection.


## -returns



If 
<b>MprAdminAcceptNewConnection</b> accepts the connection, the return value should be <b>TRUE</b>.

If 
<b>MprAdminAcceptNewConnection</b> rejects the connection, the return value should be <b>FALSE</b>.




## -remarks



RAS supports multiple Administration DLLs. RAS calls the multiple implementations of the 
<b>MprAdminAcceptNewConnection</b> function in the order in which the DLLs are listed in the 
<a href="https://msdn.microsoft.com/e83a5e37-a39d-4465-abc9-653cdd56893b">registry</a>. The remote-access user is allowed to connect only if the implementation of 
<b>MprAdminAcceptNewConnection</b> in each of the DLLs accepts the connection. In other words, every DLL must accept the connection in order for the user to be allowed to connect.

<b>Windows 2000 Server and earlier:  </b>If 
<b>MprAdminAcceptNewConnection</b> does not accept the new connection, RAS does not call the 
<a href="https://msdn.microsoft.com/504ce881-7d06-41d3-a942-0fe27be12bd3">MprAdminConnectionHangupNotification</a> function.

Do not call any of the 
<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a> or 
<a href="https://msdn.microsoft.com/e58fa4a6-16d3-4953-bf21-887d08e25af7">RAS User Administration Functions</a> from inside 
<b>MprAdminAcceptNewConnection</b>. Calls to these functions do not return when made from within a callout function.




## -see-also




<a href="https://msdn.microsoft.com/72cdcb3c-c44c-405c-ab4b-93bf9c628acf">MprAdminAcceptNewConnection2</a>



<a href="https://msdn.microsoft.com/c457b972-e326-4c6d-b146-f6ce4e18e3ea">MprAdminAcceptNewConnection3</a>



<a href="https://msdn.microsoft.com/504ce881-7d06-41d3-a942-0fe27be12bd3">MprAdminConnectionHangupNotification</a>



<a href="https://msdn.microsoft.com/3231ae83-c7fc-46d4-a4d9-f7ccf1c4ed18">MprAdminConnectionHangupNotification2</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/e2561365-be3f-44cd-bb3c-18b001fc4d5d">RAS_CONNECTION_0</a>



<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

