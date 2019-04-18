---
UID: NS:qossp._FLOWDESCRIPTOR
title: FLOWDESCRIPTOR (qossp.h)
author: windows-sdk-content
description: The FLOWDESCRIPTOR structure specifies one or more filters for a given FLOWSPEC.
old-location: qos\flowdescriptor.htm
tech.root: QOS
ms.assetid: c81a9c68-7124-4a66-9c68-d147d41c0c4d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPFLOWDESCRIPTOR, *LPFLOWDESCRIPTOR structure [QOS], FLOWDESCRIPTOR, FLOWDESCRIPTOR structure [QOS], qos.flowdescriptor, qossp/*LPFLOWDESCRIPTOR, qossp/FLOWDESCRIPTOR"
ms.topic: struct
req.header: qossp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Qossp.h
api_name:
 - FLOWDESCRIPTOR
product: Windows
targetos: Windows
req.typenames: FLOWDESCRIPTOR, *LPFLOWDESCRIPTOR
req.redist: 
ms.custom: 19H1
---

# FLOWDESCRIPTOR structure


## -description


The <b>FLOWDESCRIPTOR</b> structure specifies one or more filters for a given FLOWSPEC.


## -struct-fields




### -field FlowSpec

Flow specification (FLOWSPEC), provided as a <a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a> structure.


### -field NumFilters

Number of filters provided in <b>FilterList</b>.


### -field FilterList

Pointer to a <a href="https://msdn.microsoft.com/ce4af25d-6c31-43a2-a30a-1d28b18e8f8b">RSVP_FILTERSPEC</a> structure containing FILTERSPEC information.


## -see-also




<a href="https://msdn.microsoft.com/268e0d3a-2b04-40fd-91eb-f1780236b3e4">FLOWSPEC</a>



<a href="https://msdn.microsoft.com/ce4af25d-6c31-43a2-a30a-1d28b18e8f8b">RSVP_FILTERSPEC</a>
 

 

