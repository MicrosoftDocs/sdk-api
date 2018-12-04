---
UID: NC:winbase.PFIBER_START_ROUTINE
title: PFIBER_START_ROUTINE
author: windows-sdk-content
description: An application-defined function used with the CreateFiber function. It serves as the starting address for a fiber.
old-location: base\fiberproc.htm
tech.root: procthread
ms.assetid: 368d98f3-1ecd-47a0-98cc-0636f055ae41
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: LPFIBER_START_ROUTINE, PFIBER_START_ROUTINE, PFIBER_START_ROUTINE callback, PFIBER_START_ROUTINE callback function, _win32_fiberproc, base.fiberproc, winbase/PFIBER_START_ROUTINE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: winbase.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinBase.h
api_name:
 - PFIBER_START_ROUTINE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFIBER_START_ROUTINE callback function


## -description


An application-defined function used with the 
<a href="https://msdn.microsoft.com/3e44776b-7ef2-43fb-a2ae-e8ab7e20644b">CreateFiber</a> function. It serves as the starting address for a fiber. The <b>LPFIBER_START_ROUTINE</b> type defines a pointer to this callback function. 
<b>FiberProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param lpFiberParameter








#### - lpParameter [in]

The fiber data passed using the <i>lpParameter</i> parameter of the 
<a href="https://msdn.microsoft.com/3e44776b-7ef2-43fb-a2ae-e8ab7e20644b">CreateFiber</a> function.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/3e44776b-7ef2-43fb-a2ae-e8ab7e20644b">CreateFiber</a>



<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

