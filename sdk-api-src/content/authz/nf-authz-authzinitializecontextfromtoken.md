---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# AuthzInitializeContextFromToken function


## -description


The <b>AuthzInitializeContextFromToken</b> function initializes a client authorization context from a kernel token. The kernel token must have been opened for TOKEN_QUERY. 

Starting with Windows Server 2012 and Windows 8, this function can also copy device groups, user claims, and device claims.


## -parameters




### -param Flags [in]

Reserved for future use.


### -param TokenHandle [in]

A handle to the client token used to initialize the <i>pAuthzClientContext</i> parameter. The token must have been opened with TOKEN_QUERY access.


### -param hAuthzResourceManager [in]

A handle to the resource manager that created this client context. This handle is stored in the client context structure.


### -param pExpirationTime [in, optional]

Expiration date and time of the token. If no value is passed, the token never expires. Expiration time is not currently enforced.


### -param Identifier [in]

Identifier that is specific to the resource manager. This parameter is not currently used.


### -param DynamicGroupArgs [in, optional]

A pointer to parameters to be passed to the callback function that computes dynamic groups.


### -param phAuthzClientContext [out]

A pointer to the <i>AuthzClientContext</i> handle returned. Call 
<a href="https://msdn.microsoft.com/cad9fff0-9aa6-4cb2-a34f-94cf72f66bca">AuthzFreeContext</a> when done with the client context.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function calls the  <a href="https://msdn.microsoft.com/c20a02a0-5303-4433-a484-5a89999b32b9">AuthzComputeGroupsCallback</a> callback function to add <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> to the newly created context.




## -see-also




<a href="https://msdn.microsoft.com/cad9fff0-9aa6-4cb2-a34f-94cf72f66bca">AuthzFreeContext</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>
 

 

