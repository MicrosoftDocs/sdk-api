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

# TraceLoggingKeyword macro


## -description


Wrapper macro for setting the event's keyword(s). 


## -parameters




### -param eventKeyword [in]

The numerical keyword for the event. The value parameter must be a compile-time constant from 0 to UINT64_MAX. 


## -remarks



If no <b>TraceLoggingKeyword</b> macros are provided to a <b>TraceLoggingWrite</b> call, the event’s default keyword is 0. If multiple <b>TraceLoggingKeyword</b> macros are provided, they are OR’d together. 



