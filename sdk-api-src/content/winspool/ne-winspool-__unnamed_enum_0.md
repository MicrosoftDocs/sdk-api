---
UID: NE:winspool.__unnamed_enum_0
title: PRINT_EXECUTION_CONTEXT
author: windows-driver-content
description: Represents the execution context when GetPrintExecutionData is called.
old-location: gdi\print_execution_context.htm
old-project: printdocs
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PRINT_EXECUTION_CONTEXT, PRINT_EXECUTION_CONTEXT enumeration [Windows GDI], PRINT_EXECUTION_CONTEXT_APPLICATION, PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE, PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST, PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE, PRINT_EXECUTION_CONTEXT_WOW64, gdi.print_execution_context, winspool/PRINT_EXECUTION_CONTEXT, winspool/PRINT_EXECUTION_CONTEXT_APPLICATION, winspool/PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE, winspool/PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST, winspool/PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE, winspool/PRINT_EXECUTION_CONTEXT_WOW64
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: winspool.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRINT_EXECUTION_CONTEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINT_EXECUTION_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# PRINT_EXECUTION_CONTEXT enumeration


## -description


Represents the execution context when  <a href="https://msdn.microsoft.com/bb9506aa-a0da-46bc-a86a-84a79587cd50">GetPrintExecutionData</a> is called.


## -enum-fields




### -field PRINT_EXECUTION_CONTEXT_APPLICATION

The caller is running in an application.


### -field PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE

The caller is running in the spooler service (spoolsv.exe).


### -field PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST

The caller is running in the print isolation host (PrintIsolationHost.exe)


### -field PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE

The caller is running in the print filter pipeline (printfilterpipelinesvc.exe)


### -field PRINT_EXECUTION_CONTEXT_WOW64

The caller is running in splwow64.exe




## -see-also




<a href="https://msdn.microsoft.com/bb9506aa-a0da-46bc-a86a-84a79587cd50">GetPrintExecutionData</a>



<a href="https://msdn.microsoft.com/1fd25ed9-6f28-48f9-8132-d48fffc956ec">PRINT_EXECUTION_DATA</a>
 

 

