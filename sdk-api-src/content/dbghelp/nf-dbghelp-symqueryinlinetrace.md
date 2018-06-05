---
UID: NF:dbghelp.SymQueryInlineTrace
title: SymQueryInlineTrace function
author: windows-sdk-content
description: Queries an inline trace.
old-location: base\symqueryinlinetrace.htm
old-project: Debug
ms.assetid: e65cf979-f482-4019-ab67-5e908d23bcfa
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SymQueryInlineTrace, SymQueryInlineTrace function, base.symqueryinlinetrace, dbghelp/SymQueryInlineTrace
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: IMAGEHLP_SYMBOL_TYPE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	DbgHelp.dll
api_name:
-	SymQueryInlineTrace
product: Windows
targetos: Windows
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
---

# SymQueryInlineTrace function


## -description


Queries an inline trace.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param StartAddress [in]

The start address.


### -param StartContext [in]

Contains the context of the start of block.


### -param StartRetAddress [in]

Contains the return address of the start of the current block/


### -param CurAddress [in]

Contains the current address.


### -param CurContext [out]

Address of a <b>DWORD</b> that receives the current context.


### -param CurFrameIndex [out]

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. To retrieve extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


## -remarks



Either the <i>StartAddress</i> or <i>StartRetAddress</i> parameters must be within the same function scope as the <i>CurAddress</i> parameter. The former indicates a step-over within the same function and the latter indicates a step-over from <i>StartAddress</i>.



