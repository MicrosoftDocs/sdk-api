---
UID: NF:mprapi.MprAdminConnectionHangupNotification3
title: MprAdminConnectionHangupNotification3 function
author: windows-sdk-content
description: Remote Access Service calls the MprAdminConnectionHangupNotification3 function after the last link for the specified connection has been dismantled.
old-location: rras\mpradminconnectionhangupnotification3.htm
tech.root: RRAS
ms.assetid: 8c31d345-8f57-47f5-a021-e399f7ccca5d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MprAdminConnectionHangupNotification3, MprAdminConnectionHangupNotification3 callback, MprAdminConnectionHangupNotification3 callback function [RAS], mprapi/MprAdminConnectionHangupNotification3, rras.mpradminconnectionhangupnotification3
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
 - MprAdminConnectionHangupNotification3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminConnectionHangupNotification3 function


## -description


Remote Access Service calls the 
<b>MprAdminConnectionHangupNotification3</b> function after the last link for the specified connection has been dismantled.


## -parameters




### -param pRasConnection0 [in]

Pointer to a 
<a href="https://msdn.microsoft.com/e2561365-be3f-44cd-bb3c-18b001fc4d5d">RAS_CONNECTION_0</a> structure that describes this connection.


### -param pRasConnection1 [in]

Pointer to the 
<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a> structure that describes this connection.


### -param pRasConnection2 [in]

Pointer to a 
<a href="https://msdn.microsoft.com/5dcc20f0-7447-4256-9dde-18a4a3c95816">RAS_CONNECTION_2</a> structure that describes this connection.


### -param pRasConnection3 [in]

Pointer to a 
<a href="https://msdn.microsoft.com/f474563e-01c5-4f2a-aec4-477e0ffc7ab2">RAS_CONNECTION_3</a> structure that describes this connection.


## -returns



This function does not have a return value.




## -remarks



RAS supports multiple Administration DLLs. RAS calls the multiple implementations of the 
<b>MprAdminConnectionHangupNotification3</b> function in the order in which the DLLs are listed in the 
<a href="https://msdn.microsoft.com/e83a5e37-a39d-4465-abc9-653cdd56893b">registry</a>.

Do not call any of the 
<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a> or 
<a href="https://msdn.microsoft.com/e58fa4a6-16d3-4953-bf21-887d08e25af7">RAS User Administration Functions</a> from inside 
<b>MprAdminConnectionHangupNotification3</b>. Calls to these functions do not return when made from within a callout function.




## -see-also




<a href="https://msdn.microsoft.com/c457b972-e326-4c6d-b146-f6ce4e18e3ea">MprAdminAcceptNewConnection3</a>



<a href="https://msdn.microsoft.com/a4cbca7d-a8b0-4396-9201-648bcca6a8c8">MprAdminAcceptNewLink</a>



<a href="https://msdn.microsoft.com/504ce881-7d06-41d3-a942-0fe27be12bd3">MprAdminConnectionHangupNotification</a>



<a href="https://msdn.microsoft.com/3231ae83-c7fc-46d4-a4d9-f7ccf1c4ed18">MprAdminConnectionHangupNotification2</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/e2561365-be3f-44cd-bb3c-18b001fc4d5d">RAS_CONNECTION_0</a>



<a href="https://msdn.microsoft.com/5f6c6895-4baf-46d7-865a-b95342b70abb">RAS_CONNECTION_1</a>



<a href="https://msdn.microsoft.com/5dcc20f0-7447-4256-9dde-18a4a3c95816">RAS_CONNECTION_2</a>



<a href="https://msdn.microsoft.com/f474563e-01c5-4f2a-aec4-477e0ffc7ab2">RAS_CONNECTION_3</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

