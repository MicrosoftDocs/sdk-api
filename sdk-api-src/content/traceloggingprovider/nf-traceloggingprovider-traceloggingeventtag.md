---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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



