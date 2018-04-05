---
UID: NS:winspool.__unnamed_struct_0
title: PRINT_EXECUTION_DATA
author: windows-driver-content
description: Contains the execution context of the printer driver that calls GetPrintExecutionData.
old-location: gdi\print_execution_data.htm
old-project: printdocs
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PRINT_EXECUTION_DATA, PRINT_EXECUTION_DATA structure [Windows GDI], gdi.print_execution_data, winspool/PRINT_EXECUTION_DATA
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: PRINT_EXECUTION_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winspool.h
api_name:
-	PRINT_EXECUTION_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# PRINT_EXECUTION_DATA structure


## -description


Contains the execution context of the printer driver that calls <a href="https://msdn.microsoft.com/bb9506aa-a0da-46bc-a86a-84a79587cd50">GetPrintExecutionData</a>.


## -struct-fields




### -field context

The <a href="https://msdn.microsoft.com/b6c026b2-8519-45d3-9614-b502eec23cde">PRINT_EXECUTION_CONTEXT</a>  value that represents the current  execution context of the printer driver.


### -field clientAppPID

If the value of <b>context</b> is <b>PRINT_EXECUTION_CONTEXT_WOW64</b>, <b>clientAppPID</b> identifies the client application on whose behalf the splwow64.exe process loaded the printer driver. If  the value of <b>context</b> is not <b>PRINT_EXECUTION_CONTEXT_WOW64</b>, <b>clientAppPID</b> is zero.


## -see-also




<a href="https://msdn.microsoft.com/bb9506aa-a0da-46bc-a86a-84a79587cd50">GetPrintExecutionData</a>



<a href="https://msdn.microsoft.com/b6c026b2-8519-45d3-9614-b502eec23cde">PRINT_EXECUTION_CONTEXT</a>
 

 

