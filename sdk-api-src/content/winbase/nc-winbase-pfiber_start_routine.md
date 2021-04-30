---
UID: NC:winbase.PFIBER_START_ROUTINE
title: PFIBER_START_ROUTINE (winbase.h)
description: An application-defined function used with the CreateFiber function. It serves as the starting address for a fiber.
helpviewer_keywords: ["LPFIBER_START_ROUTINE","PFIBER_START_ROUTINE","PFIBER_START_ROUTINE callback","PFIBER_START_ROUTINE callback function","_win32_fiberproc","base.fiberproc","winbase/PFIBER_START_ROUTINE"]
old-location: base\fiberproc.htm
tech.root: backup
ms.assetid: 368d98f3-1ecd-47a0-98cc-0636f055ae41
ms.date: 12/05/2018
ms.keywords: LPFIBER_START_ROUTINE, PFIBER_START_ROUTINE, PFIBER_START_ROUTINE callback, PFIBER_START_ROUTINE callback function, _win32_fiberproc, base.fiberproc, winbase/PFIBER_START_ROUTINE
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFIBER_START_ROUTINE
 - winbase/PFIBER_START_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinBase.h
api_name:
 - PFIBER_START_ROUTINE
---

# PFIBER_START_ROUTINE callback function


## -description

An application-defined function used with the 
<a href="/windows/desktop/api/winbase/nf-winbase-createfiber">CreateFiber</a> function. It serves as the starting address for a fiber. The <b>LPFIBER_START_ROUTINE</b> type defines a pointer to this callback function. 
<b>FiberProc</b> is a placeholder for the application-defined function name.

## -parameters

### -param lpFiberParameter

#### - lpParameter [in]

The fiber data passed using the <i>lpParameter</i> parameter of the 
<a href="/windows/desktop/api/winbase/nf-winbase-createfiber">CreateFiber</a> function.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createfiber">CreateFiber</a>



<a href="/windows/desktop/ProcThread/fibers">Fibers</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>