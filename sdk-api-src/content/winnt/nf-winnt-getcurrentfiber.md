---
UID: NF:winnt.GetCurrentFiber
title: GetCurrentFiber function (winnt.h)
description: Retrieves the address of the current fiber.
helpviewer_keywords: ["GetCurrentFiber","GetCurrentFiber function","_win32_getcurrentfiber","base.getcurrentfiber","winnt/GetCurrentFiber"]
old-location: base\getcurrentfiber.htm
tech.root: ProcThread
ms.assetid: a08bfac8-00d0-41b7-9879-802189710093
ms.date: 12/05/2018
ms.keywords: GetCurrentFiber, GetCurrentFiber function, _win32_getcurrentfiber, base.getcurrentfiber, winnt/GetCurrentFiber
f1_keywords:
- winnt/GetCurrentFiber
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetCurrentFiber function


## -description


Retrieves the address of the current fiber.


## -parameters






## -returns



The macro returns the address of the currently running fiber.




## -remarks



The 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createfiber">CreateFiber</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a> functions return the fiber address when the fiber is created. The 
<b>GetCurrentFiber</b> macro allows you to retrieve the address at any other time.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-createfiber">CreateFiber</a>



<a href="https://docs.microsoft.com/windows/desktop/ProcThread/fibers">Fibers</a>
 

 

