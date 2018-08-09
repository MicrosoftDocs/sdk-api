---
UID: NC:winnt.PVECTORED_EXCEPTION_HANDLER
title: PVECTORED_EXCEPTION_HANDLER
author: windows-sdk-content
description: An application-defined function that serves as a vectored exception handler.
old-location: base\vectoredhandler.htm
old-project: debug
ms.assetid: a00f0e8d-a10b-48d4-b918-57b2ff9cb984
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PVECTORED_EXCEPTION_HANDLER, VectoredHandler, VectoredHandler callback, VectoredHandler callback function, _win32_vectoredhandler, base.vectoredhandler, winnt/VectoredHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: NUMBERFMTW, *LPNUMBERFMTW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - WinNT.h
api_name:
 - VectoredHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# PVECTORED_EXCEPTION_HANDLER callback function


## -description


An application-defined function that serves as a vectored exception handler. Specify this address when calling the 
<a href="https://msdn.microsoft.com/0e956746-e6da-49d8-a534-753cb6755673">AddVectoredExceptionHandler</a> function. The <b>PVECTORED_EXCEPTION_HANDLER</b> type defines a pointer to this callback function. 
<b>VectoredHandler</b> is a placeholder for the application-defined name.


## -parameters




### -param *ExceptionInfo [in]

A pointer to an 
<a href="https://msdn.microsoft.com/57e8cb3a-1b11-45b9-9676-3b6dc600d225">EXCEPTION_POINTERS</a> structure that receives the exception record.


## -returns



To return control to the point at which the exception occurred, return EXCEPTION_CONTINUE_EXECUTION (0xffffffff). To continue the handler search, return EXCEPTION_CONTINUE_SEARCH (0x0).




## -remarks



The handler should not call functions that acquire synchronization objects or allocate memory, because this can cause problems. Typically, the handler will simply access the exception record and return.




## -see-also




<a href="https://msdn.microsoft.com/57e8cb3a-1b11-45b9-9676-3b6dc600d225">EXCEPTION_POINTERS</a>



<a href="https://msdn.microsoft.com/e4cf8a88-1bdf-4666-8653-fe2e86c4d8ef">Vectored Exception Handling</a>
 

 

