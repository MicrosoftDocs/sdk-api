---
UID: NF:mprapi.MprAdminInitializeDllEx
title: MprAdminInitializeDllEx function (mprapi.h)
author: windows-sdk-content
description: When the Routing and Remote Access Service (RRAS) starts, it calls the MprAdminInitializeDll function that is exported by the administration DLL.
old-location: rras\mpradmininitializedllex.htm
tech.root: RRAS
ms.assetid: c608c1b3-39de-4c0f-b834-27b9211dffb5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MprAdminInitializeDllEx, MprAdminInitializeDllEx callback, MprAdminInitializeDllEx callback function [RAS], mprapi/MprAdminInitializeDllEx, rras.mpradmininitializedllex
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
 - MprAdminInitializeDllEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminInitializeDllEx function


## -description


When the Routing and Remote Access Service (RRAS) starts, it calls the 
<a href="https://msdn.microsoft.com/0a53d84e-d9be-4d18-a619-7d92c17b76bb">MprAdminInitializeDll</a> function that is exported by the administration DLL. Use this function to perform any required initialization for the DLL and call the callback functions. This serves as a placeholder for the callback functions.


## -parameters




### -param pAdminCallbacks

A pointer to a <a href="https://msdn.microsoft.com/b36036e3-1aee-41e6-b777-98455b04e44b">MPRAPI_ADMIN_DLL_CALLBACKS</a> structure that contains the function pointers of the callbacks being registered.


## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.

If the function returns any value other than <b>NO_ERROR</b>, RRAS will fail to start.




## -see-also




<a href="https://msdn.microsoft.com/0a53d84e-d9be-4d18-a619-7d92c17b76bb">MprAdminInitializeDll</a>



<a href="https://msdn.microsoft.com/7be485ce-fd45-4968-9e9d-2128d5a8967d">MprAdminTerminateDll</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

