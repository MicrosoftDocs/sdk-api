---
UID: NF:mi.MI_Class_Clone
title: MI_Class_Clone function (mi.h)
description: Clones an MI_Class object.
helpviewer_keywords: ["MI_Class_Clone","MI_Class_Clone function [Windows Management Infrastructure (MI)]","mi/MI_Class_Clone","wmi_v2.mi_class_clone"]
old-location: wmi_v2\mi_class_clone.htm
tech.root: wmi_v2
ms.assetid: a95b867c-7567-4ea4-a02c-049002de2109
ms.date: 12/05/2018
ms.keywords: MI_Class_Clone, MI_Class_Clone function [Windows Management Infrastructure (MI)], mi/MI_Class_Clone, wmi_v2.mi_class_clone
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
 - MI_Class_Clone
 - mi/MI_Class_Clone
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
 - MI_Class_Clone
---

# MI_Class_Clone function


## -description

Clones an <a href="/windows/desktop/api/mi/ns-mi-mi_class">MI_Class</a> object.

## -parameters

### -param self [in]

A pointer to the class to be cloned.

### -param newClass

A pointer to a pointer to the newly created class. When you have finished using this class, delete it by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a> function.

## -returns

This function returns MI_INLINE MI_Result MI_INLINE_CALL.

## -remarks

<b>MI_Class_Clone</b> may not create a whole new class; instead, it may refer to the original class.  Each class can be closed independent of the other, but not all of the memory is freed until all references to the class are deleted.