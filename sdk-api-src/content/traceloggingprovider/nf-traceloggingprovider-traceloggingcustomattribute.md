---
UID: NF:traceloggingprovider.TraceLoggingCustomAttribute
title: TraceLoggingCustomAttribute macro
author: windows-sdk-content
description: Wrapper macro for adding custom information about an event to the PDB.
old-location: tracelogging\traceloggingcustomattribute.htm
old-project: tracelogging
ms.assetid: D58950A3-105D-43C7-8B8B-61CC1F0D4DA0
ms.author: windowssdkdev
ms.date: 04/27/2018
ms.keywords: TraceLoggingCustomAttribute, TraceLoggingCustomAttribute macro, tracelogging.traceloggingcustomattribute, traceloggingprovider/TraceLoggingCustomAttribute
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
 - TraceLoggingCustomAttribute
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingCustomAttribute macro


## -description


Wrapper macro for adding custom information about an event to the PDB.


## -parameters




### -param key [in]

The key for the custom attribute.


### -param value [in]

The value of the custom attribute.


## -remarks



Both parameters must be string literals. This information  will appear under the CustomAttributes array for the event. If no custom  attributes are specified the array will not appear. Multiple custom attributes  can be specified per event.  

Custom attributes are stored in the PDB. They are not available at runtime.



