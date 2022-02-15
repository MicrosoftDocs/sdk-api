---
UID: NF:winnt.GetFiberData
title: GetFiberData function (winnt.h)
description: Retrieves the fiber data associated with the current fiber.
helpviewer_keywords: ["GetFiberData","GetFiberData function","_win32_getfiberdata","base.getfiberdata","winnt/GetFiberData"]
old-location: base\getfiberdata.htm
tech.root: backup
ms.assetid: 72e616ce-4188-4944-b627-9681e5fd271e
ms.date: 12/05/2018
ms.keywords: GetFiberData, GetFiberData function, _win32_getfiberdata, base.getfiberdata, winnt/GetFiberData
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetFiberData
 - winnt/GetFiberData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - GetFiberData
---

# GetFiberData function


## -description

Retrieves the fiber data associated with the current fiber.



## -returns

The macro returns the fiber data for the currently running fiber.

## -remarks

The fiber data is the value passed to the 
<a href="/windows/desktop/api/winbase/nf-winbase-createfiber">CreateFiber</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a> function in the <i>lpParameter</i> parameter. This value is also received as the parameter to the fiber function. It is stored as part of the fiber state information.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-convertthreadtofiber">ConvertThreadToFiber</a>



<a href="/windows/desktop/api/winbase/nf-winbase-createfiber">CreateFiber</a>



<a href="/windows/desktop/ProcThread/fibers">Fibers</a>
