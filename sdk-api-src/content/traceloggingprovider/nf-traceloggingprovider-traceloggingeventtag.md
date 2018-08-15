---
UID: NF:traceloggingprovider.TraceLoggingEventTag
title: TraceLoggingEventTag macro
author: windows-sdk-content
description: Wrapper macro for setting the event's tag(s).
old-location: tracelogging\traceloggingeventtag.htm
old-project: tracelogging
ms.assetid: D7BD0AC7-2330-4DE7-8C46-CF210B102704
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TraceLoggingEventTag, TraceLoggingEventTag macro, tracelogging.traceloggingeventtag, traceloggingprovider/TraceLoggingEventTag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: traceloggingprovider.h
req.include-header: 
req.redist: 
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
 - TraceLoggingEventTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# TraceLoggingEventTag macro


## -description


Wrapper macro for setting the event's tag(s).  


## -parameters




### -param eventTag [in]

A compile-time constant in the range of 0x00200000-0x0FE00000.


## -remarks



 The semantics of the tags are defined by the event consumer.  During event processing, this tag can be retrieved from the <a href="https://msdn.microsoft.com/ecf57a23-0dd2-4954-82ac-e92f651c226f">TRACE_EVENT_INFO</a>  Tags field.    

The TraceLogging schema convention encodes tags as 28-bit fields by using a  chain of up to four bytes with the upper-most bit used as a 'chain' bit  (4*7 = 28). Data is encoded most-significant byte first.  <a href="https://msdn.microsoft.com/BFBC6802-64DC-478E-B09D-F550135994AB">TraceLoggingWrite</a> and TraceLoggingEventTag only supports encoding a single  byte of tag data, which must then contain the upper-most range of seven bits,  thus 0x0FE00000. 

If no parameters are provided, no tag is transmitted for the  event. If multiple args are provided, they are OR'ed  together.  



