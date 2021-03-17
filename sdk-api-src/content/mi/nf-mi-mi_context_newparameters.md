---
UID: NF:mi.MI_Context_NewParameters
title: MI_Context_NewParameters function (mi.h)
description: Creates a new instance of a method given a method declaration.
helpviewer_keywords: ["MI_Context_NewParameters","MI_Context_NewParameters function [Windows Management Infrastructure (MI)]","mi/MI_Context_NewParameters","wmi.mi_newparameters","wmi_v2.mi_context_newparameters"]
old-location: wmi_v2\mi_context_newparameters.htm
tech.root: wmi_v2
ms.assetid: 8fb80e6f-627c-4897-9776-7454c0258809
ms.date: 12/05/2018
ms.keywords: MI_Context_NewParameters, MI_Context_NewParameters function [Windows Management Infrastructure (MI)], mi/MI_Context_NewParameters, wmi.mi_newparameters, wmi_v2.mi_context_newparameters
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
 - MI_Context_NewParameters
 - mi/MI_Context_NewParameters
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
 - MI_Context_NewParameters
---

# MI_Context_NewParameters function


## -description

Creates a new instance of a method given a method declaration.

## -parameters

### -param context [in]

A pointer to the request context.

### -param methodDecl [in]

A pointer to the Method declaration used to initialize the instance.

### -param instance

A pointer to the returned instance.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

When you are finished using the instance, it must be deleted with the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a> function.