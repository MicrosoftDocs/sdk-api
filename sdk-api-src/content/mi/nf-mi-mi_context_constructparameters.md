---
UID: NF:mi.MI_Context_ConstructParameters
title: MI_Context_ConstructParameters function (mi.h)
description: A provider calls this function to initialize a parameter's instance.
helpviewer_keywords: ["MI_Context_ConstructParameters","MI_Context_ConstructParameters function [Windows Management Infrastructure (MI)]","mi/MI_Context_ConstructParameters","wmi.mi_constructparameters","wmi_v2.mi_context_constructparameters"]
old-location: wmi_v2\mi_context_constructparameters.htm
tech.root: wmi_v2
ms.assetid: dd5bea1c-fee0-4ebf-9c4c-a42bf9ba315b
ms.date: 12/05/2018
ms.keywords: MI_Context_ConstructParameters, MI_Context_ConstructParameters function [Windows Management Infrastructure (MI)], mi/MI_Context_ConstructParameters, wmi.mi_constructparameters, wmi_v2.mi_context_constructparameters
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
 - MI_Context_ConstructParameters
 - mi/MI_Context_ConstructParameters
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
 - MI_Context_ConstructParameters
---

# MI_Context_ConstructParameters function


## -description

A provider calls this function to initialize a parameter's instance.

## -parameters

### -param context [in]

A pointer to the request context.

### -param methodDecl [in]

A pointer to the method declaration used to initialize the instance.

### -param instance [out]

A pointer to the returned instance.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -remarks

You are responsible for reserving the memory for the instance (either on the stack or the heap). When you have finished using the instance, delete it by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_destruct">MI_Instance_Destruct</a> function.