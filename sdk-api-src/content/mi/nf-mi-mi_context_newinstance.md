---
UID: NF:mi.MI_Context_NewInstance
title: MI_Context_NewInstance function (mi.h)
description: Creates a new instance of a class given a class declaration.
helpviewer_keywords: ["MI_Context_NewInstance","MI_Context_NewInstance function [Windows Management Infrastructure (MI)]","mi/MI_Context_NewInstance","wmi.mi_newinstance","wmi_v2.mi_context_newinstance"]
old-location: wmi_v2\mi_context_newinstance.htm
tech.root: wmi_v2
ms.assetid: 59571aa0-7fc2-4724-94e8-15b8a62327b6
ms.date: 12/05/2018
ms.keywords: MI_Context_NewInstance, MI_Context_NewInstance function [Windows Management Infrastructure (MI)], mi/MI_Context_NewInstance, wmi.mi_newinstance, wmi_v2.mi_context_newinstance
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
 - MI_Context_NewInstance
 - mi/MI_Context_NewInstance
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
 - MI_Context_NewInstance
---

# MI_Context_NewInstance function


## -description

Creates a new instance of a class given a class declaration.

## -parameters

### -param context [in]

A pointer to the request context.

### -param classDecl [in]

A pointer to the class declaration used to initialize the instance. The runtime type information (RTTI) is generated for the class and should be named for the class, followed by an "_rtti" suffix.

### -param instance

A pointer to the returned instance. There is also a generated function named for the class, followed by a  "_Delete" suffix.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.

## -remarks

When you are finished using the instance, it must be deleted via the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a> function.