---
UID: NS:evntrace._CLASSIC_EVENT_ID
title: "_CLASSIC_EVENT_ID"
author: windows-sdk-content
description: Identifies the kernel event for which you want to enable call stack tracing.
old-location: etw\classic_event_id.htm
tech.root: ETW
ms.assetid: cbd77002-466b-40e6-85a5-cd872aef7d51
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PCLASSIC_EVENT_ID, CLASSIC_EVENT_ID, CLASSIC_EVENT_ID structure [ETW], PCLASSIC_EVENT_ID, PCLASSIC_EVENT_ID structure pointer [ETW], _CLASSIC_EVENT_ID, etw.classic_event_id, evntrace/CLASSIC_EVENT_ID, evntrace/PCLASSIC_EVENT_ID"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntrace.h
api_name:
 - CLASSIC_EVENT_ID
product: Windows
targetos: Windows
req.typenames: CLASSIC_EVENT_ID, *PCLASSIC_EVENT_ID
req.redist: 
---

# _CLASSIC_EVENT_ID structure


## -description


Identifies the kernel event for  which you want to enable call stack tracing.


## -struct-fields




### -field EventGuid

The GUID that identifies the kernel event class.


### -field Type

The event type that identifies the event within the kernel event class to enable.


### -field Reserved

Reserved.


## -remarks



To enable the <a href="https://msdn.microsoft.com/fe7d4efa-3d39-4438-a1a6-af3f65ea3deb">read</a> event type for <a href="https://msdn.microsoft.com/630fb6c6-b505-4384-ab7b-ee898d95bd41">disk IO </a>events, set <b>GUID</b> to 3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c and <b>Type</b> to 10.




## -see-also




<a href="https://msdn.microsoft.com/f4cdbe32-6885-4844-add5-560961c3dd1d">TraceSetInformation</a>
 

 

