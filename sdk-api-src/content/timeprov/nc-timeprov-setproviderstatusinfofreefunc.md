---
UID: NC:timeprov.SetProviderStatusInfoFreeFunc
title: SetProviderStatusInfoFreeFunc
author: windows-sdk-content
description: Frees a SetProviderStatusInfo structure.
old-location: base\setproviderstatusinfofreefunc.htm
old-project: SysInfo
ms.assetid: ea26aa92-af2a-4764-934d-2a21989a216f
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: SetProviderStatusInfoFreeFunc, SetProviderStatusInfoFreeFunc callback, SetProviderStatusInfoFreeFunc callback function, _win32_setproviderstatusinfofreefunc, base.setproviderstatusinfofreefunc, timeprov/SetProviderStatusInfoFreeFunc
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: timeprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: TIMECAPS, *PTIMECAPS, *NPTIMECAPS, *LPTIMECAPS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Timeprov.h
api_name:
 - SetProviderStatusInfoFreeFunc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# SetProviderStatusInfoFreeFunc callback function


## -description


Frees a 
<a href="https://msdn.microsoft.com/8e0a79ba-f76a-435a-9b0b-c3a2d9c390da">SetProviderStatusInfo</a> structure.


## -parameters




### -param *pspsi [in]

A pointer to the 
<a href="https://msdn.microsoft.com/8e0a79ba-f76a-435a-9b0b-c3a2d9c390da">SetProviderStatusInfo</a> structure to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/e52dd1d3-081a-4fcc-85d9-a1dcef0e8011">SetProviderStatusFunc</a>



<a href="https://msdn.microsoft.com/8e0a79ba-f76a-435a-9b0b-c3a2d9c390da">SetProviderStatusInfo</a>
 

 

