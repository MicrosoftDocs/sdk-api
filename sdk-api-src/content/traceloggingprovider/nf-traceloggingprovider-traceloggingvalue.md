---
UID: NF:traceloggingprovider.TraceLoggingValue
title: TraceLoggingValue macro
author: windows-sdk-content
description: Wrapper macro for event fields. Automatically deduces value type.
old-location: tracelogging\traceloggingvalue.htm
old-project: tracelogging
ms.assetid: F4013632-3DC8-413C-B25F-64DE070FA4A8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TraceLoggingValue, TraceLoggingValue macro, tracelogging.traceloggingvalue, traceloggingprovider/TraceLoggingValue
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
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - traceloggingprovider.h
api_name:
 - TraceLoggingValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingValue macro


## -description


Wrapper macro for event fields. Automatically deduces value type.


## -parameters




### -param value [in]

The event field value.


#### - name [in, optional]

The name of the event field. If provided, the name parameter must be a string literal (not a variable) and must not  contain any '\0' characters.


#### - description [in, optional]

The description of the event field's value. If provided, the description parameter must be a string literal, and will be included in the PDB. 


#### - tags [in, optional]

An integer value. The low 28 bits of the value will be included in the field's metadata. The semantics of the tags  are defined by the event consumer. During event processing, this tag can be retrieved from the EVENT_PROPERTY_INFO Tags field. 

