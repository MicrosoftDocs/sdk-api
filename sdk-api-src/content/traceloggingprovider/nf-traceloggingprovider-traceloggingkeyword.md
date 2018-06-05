---
UID: NF:traceloggingprovider.TraceLoggingKeyword
title: TraceLoggingKeyword macro
author: windows-sdk-content
description: Wrapper macro for setting the event's keyword(s).
old-location: tracelogging\traceloggingkeyword.htm
old-project: tracelogging
ms.assetid: 4837DCE3-929F-458B-95E1-8720FD3E9FFA
ms.author: windowssdkdev
ms.date: 04/26/2018
ms.keywords: TraceLoggingKeyword, TraceLoggingKeyword macro, tracelogging.traceloggingkeyword, traceloggingprovider/TraceLoggingKeyword
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: traceloggingprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2
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
req.typenames: TPMVSCMGR_ERROR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	traceloggingprovider.h
api_name:
-	TraceLoggingKeyword
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingKeyword macro


## -description


Wrapper macro for setting the event's keyword(s). 


## -parameters




### -param eventKeyword [in]

The numerical keyword for the event. The value parameter must be a compile-time constant from 0 to UINT64_MAX. 


## -remarks



If no <b>TraceLoggingKeyword</b> macros are provided to a <b>TraceLoggingWrite</b> call, the event’s default keyword is 0. If multiple <b>TraceLoggingKeyword</b> macros are provided, they are OR’d together. 



