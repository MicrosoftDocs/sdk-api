---
UID: NE:tdh._TEMPLATE_FLAGS
title: "_TEMPLATE_FLAGS"
author: windows-sdk-content
description: Defines constant values that indicates the layout of the event data.
old-location: etw\template_flags_enum.htm
tech.root: ETW
ms.assetid: 07132dc2-fad9-4ddb-bf46-70a887f0b585
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: TEMPLATE_EVENT_DATA, TEMPLATE_FLAGS, TEMPLATE_FLAGS enumeration [ETW], TEMPLATE_USER_DATA, _TEMPLATE_FLAGS, etw.template_flags_enum, tdh.template_flags_enum, tdh/TEMPLATE_EVENT_DATA, tdh/TEMPLATE_FLAGS, tdh/TEMPLATE_USER_DATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: TEMPLATE_FLAGS
req.redist: 
---

# _TEMPLATE_FLAGS enumeration


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




<a href="https://msdn.microsoft.com/ecf57a23-0dd2-4954-82ac-e92f651c226f">TRACE_EVENT_INFO</a>
 

 

