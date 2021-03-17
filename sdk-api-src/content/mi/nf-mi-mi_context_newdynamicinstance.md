---
UID: NF:mi.MI_Context_NewDynamicInstance
title: MI_Context_NewDynamicInstance function (mi.h)
description: Creates a new dynamic instance (weakly typed instance without a class declaration) of a class.
helpviewer_keywords: ["MI_Context_NewDynamicInstance","MI_Context_NewDynamicInstance function [Windows Management Infrastructure (MI)]","mi/MI_Context_NewDynamicInstance","wmi.mi_newdynamicinstance","wmi_v2.mi_context_newdynamicinstance"]
old-location: wmi_v2\mi_context_newdynamicinstance.htm
tech.root: wmi_v2
ms.assetid: 05415945-c804-4056-b4bf-673995c1d6e4
ms.date: 12/05/2018
ms.keywords: MI_Context_NewDynamicInstance, MI_Context_NewDynamicInstance function [Windows Management Infrastructure (MI)], mi/MI_Context_NewDynamicInstance, wmi.mi_newdynamicinstance, wmi_v2.mi_context_newdynamicinstance
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Context_NewDynamicInstance
 - mi/MI_Context_NewDynamicInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Context_NewDynamicInstance
---

# MI_Context_NewDynamicInstance function


## -description

Creates a new dynamic instance (weakly typed instance without a class declaration) of a class.

## -parameters

### -param context [in]

A pointer to the request context.

### -param className [in]

The name of the new class.

### -param flags

The create flags (include class meta type).

### -param instance

A pointer to a new instance upon successful return.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -remarks

To add elements, call the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_addelement">MI_Instance_AddElement</a> function. When you have finished using the instance, delete it with the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a> function.

## -see-also

<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_addelement">MI_Instance_AddElement</a>



<a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a>