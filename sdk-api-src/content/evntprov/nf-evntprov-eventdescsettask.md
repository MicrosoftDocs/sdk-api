---
UID: NF:evntprov.EventDescSetTask
title: EventDescSetTask function
author: windows-sdk-content
description: Sets the Task member of the event descriptor.
old-location: etw\eventdescsettask_func.htm
old-project: ETW
ms.assetid: 74298e6f-b29a-4fa7-98d1-f81270fcbc0e
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: EventDescSetTask, EventDescSetTask function [ETW], base.eventdescsettask_func, etw.eventdescsettask_func, evntprov/EventDescSetTask
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: EVENT_INFO_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Evntprov.h
api_name:
-	EventDescSetTask
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventDescSetTask function


## -description


Sets the <b>Task</b> member of the event descriptor.


## -parameters




### -param EventDescriptor [in]

Event descriptor to modify. See <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param Task [in]

Task that identifies the logical component of the application whose events you want to enable.


## -returns



The modified event descriptor.




## -remarks



This is a convenience macro for setting the member of the <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>
 

 

