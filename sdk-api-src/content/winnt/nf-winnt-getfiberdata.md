---
UID: NF:winnt.GetFiberData
title: GetFiberData function (winnt.h)
author: windows-sdk-content
description: Retrieves the fiber data associated with the current fiber.
old-location: base\getfiberdata.htm
tech.root: ProcThread
ms.assetid: 72e616ce-4188-4944-b627-9681e5fd271e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFiberData, GetFiberData function, _win32_getfiberdata, base.getfiberdata, winnt/GetFiberData
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
 - GetFiberData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetFiberData function


## -description


Retrieves the fiber data associated with the current fiber.


## -parameters






## -returns



The macro returns the fiber data for the currently running fiber.




## -remarks



The fiber data is the value passed to the 
<a href="https://msdn.microsoft.com/3e44776b-7ef2-43fb-a2ae-e8ab7e20644b">CreateFiber</a> or 
<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a> function in the <i>lpParameter</i> parameter. This value is also received as the parameter to the fiber function. It is stored as part of the fiber state information.




## -see-also




<a href="https://msdn.microsoft.com/31954a7e-b9a3-4d60-b43a-54fe0047f380">ConvertThreadToFiber</a>



<a href="https://msdn.microsoft.com/3e44776b-7ef2-43fb-a2ae-e8ab7e20644b">CreateFiber</a>



<a href="https://msdn.microsoft.com/6283f56b-23ae-4840-abd0-2478a50c670c">Fibers</a>
 

 

