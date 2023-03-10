---
UID: NF:mi.MI_Context_ConstructInstance
title: MI_Context_ConstructInstance function (mi.h)
description: Initializes an MI class instance on the stack or as a member of a structure.
helpviewer_keywords: ["MI_Context_ConstructInstance","MI_Context_ConstructInstance function [Windows Management Infrastructure (MI)]","mi/MI_Context_ConstructInstance","wmi.mi_constructinstance","wmi_v2.mi_context_constructinstance"]
old-location: wmi_v2\mi_context_constructinstance.htm
tech.root: wmi_v2
ms.assetid: c1b90938-401a-4fae-99de-9954d02b892e
ms.date: 12/05/2018
ms.keywords: MI_Context_ConstructInstance, MI_Context_ConstructInstance function [Windows Management Infrastructure (MI)], mi/MI_Context_ConstructInstance, wmi.mi_constructinstance, wmi_v2.mi_context_constructinstance
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
 - MI_Context_ConstructInstance
 - mi/MI_Context_ConstructInstance
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
 - MI_Context_ConstructInstance
---

# MI_Context_ConstructInstance function


## -description

Initializes an MI class instance on the stack or as a member of a structure.

## -parameters

### -param context [in]

A pointer to the request context.

### -param classDecl [in]

A pointer to the class declaration used to initialize the instance.

### -param instance [out]

A pointer to the returned instance.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -remarks

You are responsible for reserving the memory for the instance (either on the stack or the heap). When you have finished using the instance, delete it by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_destruct">MI_Instance_Destruct</a> function.