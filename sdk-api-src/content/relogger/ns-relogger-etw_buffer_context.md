---
UID: NS:relogger._ETW_BUFFER_CONTEXT
title: ETW_BUFFER_CONTEXT (relogger.h)
description: Provides context information about the event. (ETW_BUFFER_CONTEXT)
helpviewer_keywords: ["*PETW_BUFFER_CONTEXT","ETW_BUFFER_CONTEXT","ETW_BUFFER_CONTEXT structure [ETW]","PETW_BUFFER_CONTEXT","PETW_BUFFER_CONTEXT structure pointer [ETW]","_ETW_BUFFER_CONTEXT","base.etw_buffer_context","etw.etw_buffer_context","relogger/ETW_BUFFER_CONTEXT","relogger/PETW_BUFFER_CONTEXT"]
old-location: etw\etw_buffer_context.htm
tech.root: ETW
ms.assetid: 75577305-fb3f-40a2-8fe6-9cd82c3f4e69
ms.date: 12/05/2018
ms.keywords: '*PETW_BUFFER_CONTEXT, ETW_BUFFER_CONTEXT, ETW_BUFFER_CONTEXT structure [ETW], PETW_BUFFER_CONTEXT, PETW_BUFFER_CONTEXT structure pointer [ETW], _ETW_BUFFER_CONTEXT, base.etw_buffer_context, etw.etw_buffer_context, relogger/ETW_BUFFER_CONTEXT, relogger/PETW_BUFFER_CONTEXT'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ETW_BUFFER_CONTEXT, *PETW_BUFFER_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ETW_BUFFER_CONTEXT
 - relogger/_ETW_BUFFER_CONTEXT
 - PETW_BUFFER_CONTEXT
 - relogger/PETW_BUFFER_CONTEXT
 - ETW_BUFFER_CONTEXT
 - relogger/ETW_BUFFER_CONTEXT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - relogger.h
api_name:
 - ETW_BUFFER_CONTEXT
---

# ETW_BUFFER_CONTEXT structure


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

<a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a>
