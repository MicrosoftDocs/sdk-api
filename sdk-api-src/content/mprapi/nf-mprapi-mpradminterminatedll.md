---
UID: NF:mprapi.MprAdminTerminateDll
title: MprAdminTerminateDll function
author: windows-sdk-content
description: When the RAS shuts down, it calls the MprAdminTerminateDll function exported by the administration DLL. Use this function to perform any required clean-up for the DLL.
old-location: rras\mpradminterminatedll.htm
tech.root: rras
ms.assetid: 7be485ce-fd45-4968-9e9d-2128d5a8967d
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MprAdminTerminateDll, MprAdminTerminateDll callback, MprAdminTerminateDll callback function [RAS], _mpr_mpradminterminatedll, mprapi/MprAdminTerminateDll, rras.mpradminterminatedll
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - MprAdminTerminateDll
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MprAdminTerminateDll function


## -description


When the RAS shuts down, it calls the 
<b>MprAdminTerminateDll</b> function exported by the administration DLL. Use this function to perform any required clean-up for the DLL.


## -parameters






## -returns



If the function succeeds, the return value is <b>NO_ERROR</b>.




## -remarks



RAS supports multiple Administration DLLs. RAS calls the multiple implementations of <a href="https://msdn.microsoft.com/0a53d84e-d9be-4d18-a619-7d92c17b76bb">MprAdminInitializeDll</a> in the order in which the DLLs are listed in the 
<a href="https://msdn.microsoft.com/e83a5e37-a39d-4465-abc9-653cdd56893b">registry</a>.




## -see-also




<a href="https://msdn.microsoft.com/0a53d84e-d9be-4d18-a619-7d92c17b76bb">MprAdminInitializeDll</a>



<a href="https://msdn.microsoft.com/c15c6e2d-3bb6-4583-9ac3-19528feb863f">RAS Administration DLL</a>



<a href="https://msdn.microsoft.com/27cf63e2-9dd3-4bc1-98af-e93055d89492">RAS Administration Functions</a>



<a href="https://msdn.microsoft.com/6170fcf2-26d5-4418-bddb-2afd99510520">Remote Access Service Administration Reference</a>
 

 

