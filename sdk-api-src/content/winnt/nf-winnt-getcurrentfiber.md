---
UID: NF:winnt.GetCurrentFiber
title: GetCurrentFiber function
author: windows-sdk-content
description: Retrieves the address of the current fiber.
old-location: base\getcurrentfiber.htm
tech.root: procthread
ms.assetid: a08bfac8-00d0-41b7-9879-802189710093
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetCurrentFiber, GetCurrentFiber function, _win32_getcurrentfiber, base.getcurrentfiber, winnt/GetCurrentFiber
ms.topic: function
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - GetCurrentFiber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetCurrentFiber function


## -description


Retrieves the address of the current fiber.


## -parameters






## -returns



The macro returns the address of the currently running fiber.




## -remarks



The 
<a href="https://msdn.microsoft.com/3e44776b-7ef2-43fb-a2ae-e8ab7e20644b">CreateFiber</a> and 
<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a> functions return the fiber address when the fiber is created. The 
<b>GetCurrentFiber</b> macro allows you to retrieve the address at any other time.




## -see-also




<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a>



<a href="https://msdn.microsoft.com/3e44776b-7ef2-43fb-a2ae-e8ab7e20644b">CreateFiber</a>



<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>
 

 

