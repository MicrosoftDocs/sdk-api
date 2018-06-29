---
UID: NS:relogger._ETW_BUFFER_CONTEXT
title: "_ETW_BUFFER_CONTEXT"
author: windows-sdk-content
description: Provides context information about the event.
old-location: etw\etw_buffer_context.htm
old-project: ETW
ms.assetid: 75577305-fb3f-40a2-8fe6-9cd82c3f4e69
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PETW_BUFFER_CONTEXT, ETW_BUFFER_CONTEXT, ETW_BUFFER_CONTEXT structure [ETW], PETW_BUFFER_CONTEXT, PETW_BUFFER_CONTEXT structure pointer [ETW], _ETW_BUFFER_CONTEXT, base.etw_buffer_context, etw.etw_buffer_context, relogger/ETW_BUFFER_CONTEXT, relogger/PETW_BUFFER_CONTEXT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: relogger.h
req.include-header: Evntrace.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Relogger.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ETW_BUFFER_CONTEXT, *PETW_BUFFER_CONTEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - relogger.h
api_name:
 - ETW_BUFFER_CONTEXT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _ETW_BUFFER_CONTEXT structure


## -description


The <b>ETW_BUFFER_CONTEXT</b> structure provides context information about the event.


## -struct-fields




### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

 


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.ProcessorNumber

The number of the CPU on which the provider process was running. The number is zero on a single processor computer.


### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.Alignment

Alignment between events (always eight).


### -field DUMMYUNIONNAME.ProcessorIndex

 


### -field LoggerId

Identifier of the session that logged the event.


## -see-also




<a href="https://msdn.microsoft.com/e352c1a7-39a2-43e3-a723-5fc6a3921ee8">EVENT_RECORD</a>
 

 

