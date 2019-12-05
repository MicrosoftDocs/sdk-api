---
UID: NE:tdh._TEMPLATE_FLAGS
title: TEMPLATE_FLAGS (tdh.h)
description: Defines constant values that indicates the layout of the event data.
old-location: etw\template_flags_enum.htm
tech.root: ETW
ms.assetid: 07132dc2-fad9-4ddb-bf46-70a887f0b585
ms.date: 12/05/2018
ms.keywords: TEMPLATE_EVENT_DATA, TEMPLATE_FLAGS, TEMPLATE_FLAGS enumeration [ETW], TEMPLATE_USER_DATA, etw.template_flags_enum, tdh.template_flags_enum, tdh/TEMPLATE_EVENT_DATA, tdh/TEMPLATE_FLAGS, tdh/TEMPLATE_USER_DATA
ms.topic: enum
f1_keywords:
- tdh/TEMPLATE_FLAGS
dev_langs:
- c++
req.header: tdh.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Tdh.h
api_name:
- TEMPLATE_FLAGS
targetos: Windows
req.typenames: TEMPLATE_FLAGS
req.redist: 
ms.custom: 19H1
---

# TEMPLATE_FLAGS enumeration


## -description


Defines constant values that
		indicates the layout of the event data.


## -enum-fields




### -field TEMPLATE_EVENT_DATA

The layout of the event data is determined by the order of the data items defined in the event data template definition.


### -field TEMPLATE_USER_DATA

The layout of the event data is determined by the XML fragment included in the event data template definition.


### -field TEMPLATE_CONTROL_GUID




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-trace_event_info">TRACE_EVENT_INFO</a>
 

 

