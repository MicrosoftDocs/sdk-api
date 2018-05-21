---
UID: NS:mi._MI_Context
title: "_MI_Context"
author: windows-driver-content
description: Holds context for the operation that the provider needs to carry out.
old-location: wmi_v2\mi_context.htm
old-project: wmi_v2
ms.assetid: 51d6c510-f9fd-4ab7-a669-b2a5776b496d
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: MI_Context, MI_Context structure [Windows Management Infrastructure (MI)], _MI_Context, mi/MI_Context, wmi._mi_context, wmi_v2.mi_context
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MI_Context
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Mi.h
api_name:
-	MI_Context
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MI_Context structure


## -description


Holds context for the operation that the provider needs to carry out.  There are a set of MI_Context_* APIs to perform such actions as reporting operation results and retrieving the options/settings associated with an operation.  The context object is valid only until the final result for the operation is sent.


## -struct-fields




### -field ft

This member is used internally, and it must not be changed.


### -field reserved

Reserved for internal use.

