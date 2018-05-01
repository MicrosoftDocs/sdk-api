---
UID: NS:avrfsdk._AVRF_HANDLE_OPERATION
title: "_AVRF_HANDLE_OPERATION"
author: windows-driver-content
description: Contains information required to collect handle trace information.
old-location: winprog\avrf_handle_operation.htm
old-project: DevNotes
ms.assetid: 9268d24d-5000-4ac5-a3c5-895613ccbb9a
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: "*PAVRF_HANDLE_OPERATION, AVRF_HANDLE_OPERATION, AVRF_HANDLE_OPERATION structure [Windows API], _AVRF_HANDLE_OPERATION, avrfsdk/AVRF_HANDLE_OPERATION, base.avrf_handle_operation, winprog.avrf_handle_operation"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: avrfsdk.h
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
req.typenames: AVRF_HANDLE_OPERATION, *PAVRF_HANDLE_OPERATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Avrfsdk.h
api_name:
-	AVRF_HANDLE_OPERATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _AVRF_HANDLE_OPERATION structure


## -description


Contains information required to collect handle trace information.


## -struct-fields




### -field Handle

The handle to the heap in which handle traces are being enumerated.


### -field ProcessId

A unique identifier associated with the process in which the application is running.


### -field ThreadId

A unique identifier of the thread (returned by the <a href="https://msdn.microsoft.com/library/windows/hardware/ff546542">GetCurrentThreadId</a> function) that has performed an operation on the given handle.


### -field OperationType

One of the constants in the <a href="https://msdn.microsoft.com/bcaaa52a-8eb1-4ad7-9ee5-97cca91a2238">eHANDLE_TRACE_OPERATIONS</a> enum that indicate whether the handle operation is                  an open(create), close, or invalid.  


### -field Spare0

The alignment of the structure on a natural boundary even if the user has changed the size of the original structure.


### -field BackTraceInformation

Identifies the <a href="https://msdn.microsoft.com/634d9569-469c-4dc7-9192-217af0937b6c">AVRF_BACKTRACE_INFORMATION</a> structure containing information required for completing the enumeration of handles.


## -see-also




<a href="https://msdn.microsoft.com/99cb9005-9cfc-44fb-b09f-fed0541cda37">Resource Enumeration</a>



<a href="https://msdn.microsoft.com/e1715f2a-5928-44e6-afbf-f2f0ab0ba3dd">VerifierEnumerateResource</a>
 

 

