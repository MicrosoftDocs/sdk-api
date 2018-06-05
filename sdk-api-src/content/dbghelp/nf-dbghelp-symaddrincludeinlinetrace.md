---
UID: NF:dbghelp.SymAddrIncludeInlineTrace
title: SymAddrIncludeInlineTrace function
author: windows-sdk-content
description: Indicates whether the specified address is within an inline frame.
old-location: base\symaddrincludeinlinetrace.htm
old-project: Debug
ms.assetid: 12bb0fbf-3573-4efd-88a6-e94828906413
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: SymAddrIncludeInlineTrace, SymAddrIncludeInlineTrace function, base.symaddrincludeinlinetrace, dbghelp/SymAddrIncludeInlineTrace
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
-	SymAddrIncludeInlineTrace
product: Windows
targetos: Windows
req.lib: DbgHelp.lib
req.dll: DbgHelp.dll
req.irql: 
---

# SymAddrIncludeInlineTrace function


## -description


Indicates whether the specified address is within an inline frame.


## -parameters




### -param hProcess [in]

A handle to a process. This handle must have been previously passed to the 
      <a href="https://msdn.microsoft.com/fb1c98cb-6cd0-4218-aea4-384c24c66395">SymInitialize</a> function.


### -param Address [in]

The address.


## -returns



Returns zero if the address is not within an inline frame.



