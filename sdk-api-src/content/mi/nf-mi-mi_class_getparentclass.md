---
UID: NF:mi.MI_Class_GetParentClass
title: MI_Class_GetParentClass function (mi.h)
description: Gets the parent class for the specified class.
helpviewer_keywords: ["MI_Class_GetParentClass","MI_Class_GetParentClass function [Windows Management Infrastructure (MI)]","mi/MI_Class_GetParentClass","wmi_v2.mi_class_getparentclass"]
old-location: wmi_v2\mi_class_getparentclass.htm
tech.root: wmi_v2
ms.assetid: e90e3072-7d01-4959-bfee-c85ea89775a2
ms.date: 12/05/2018
ms.keywords: MI_Class_GetParentClass, MI_Class_GetParentClass function [Windows Management Infrastructure (MI)], mi/MI_Class_GetParentClass, wmi_v2.mi_class_getparentclass
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
 - MI_Class_GetParentClass
 - mi/MI_Class_GetParentClass
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
 - MI_Class_GetParentClass
---

# MI_Class_GetParentClass function


## -description

Gets the parent class for the specified class.

## -parameters

### -param self [in]

A pointer to the child class.

### -param parentClass

A pointer to a pointer to the returned parent class. When you have finished using the class, deleted it by using the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a> function.

## -returns

This function returns MI_INLINE MI_Result.