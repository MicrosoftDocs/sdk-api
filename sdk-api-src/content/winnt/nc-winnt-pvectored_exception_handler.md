---
UID: NC:winnt.PVECTORED_EXCEPTION_HANDLER
title: PVECTORED_EXCEPTION_HANDLER (winnt.h)
description: An application-defined function that serves as a vectored exception handler.
helpviewer_keywords: ["PVECTORED_EXCEPTION_HANDLER","VectoredHandler","VectoredHandler callback","VectoredHandler callback function","_win32_vectoredhandler","base.vectoredhandler","winnt/VectoredHandler"]
old-location: base\vectoredhandler.htm
tech.root: Debug
ms.assetid: a00f0e8d-a10b-48d4-b918-57b2ff9cb984
ms.date: 12/05/2018
ms.keywords: PVECTORED_EXCEPTION_HANDLER, VectoredHandler, VectoredHandler callback, VectoredHandler callback function, _win32_vectoredhandler, base.vectoredhandler, winnt/VectoredHandler
req.header: winnt.h
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
 - PVECTORED_EXCEPTION_HANDLER
 - winnt/PVECTORED_EXCEPTION_HANDLER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinNT.h
api_name:
 - VectoredHandler
---

# PVECTORED_EXCEPTION_HANDLER callback function


## -description

An application-defined function that serves as a vectored exception handler. Specify this address when calling the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler">AddVectoredExceptionHandler</a> function. The <b>PVECTORED_EXCEPTION_HANDLER</b> type defines a pointer to this callback function. 
<b>VectoredHandler</b> is a placeholder for the application-defined name.

## -parameters

### -param ExceptionInfo [in]

A pointer to an 
<a href="/windows/desktop/api/winnt/ns-winnt-exception_pointers">EXCEPTION_POINTERS</a> structure that receives the exception record.

## -returns

To return control to the point at which the exception occurred, return EXCEPTION_CONTINUE_EXECUTION (0xffffffff). To continue the handler search, return EXCEPTION_CONTINUE_SEARCH (0x0).

## -remarks

The handler should not call functions that acquire synchronization objects or allocate memory, because this can cause problems. Typically, the handler will simply access the exception record and return.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-exception_pointers">EXCEPTION_POINTERS</a>



<a href="/windows/desktop/Debug/vectored-exception-handling">Vectored Exception Handling</a>
