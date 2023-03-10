---
UID: NF:mi.MI_Class_GetParentClassName
title: MI_Class_GetParentClassName function (mi.h)
description: Gets the parent class name of the specified class.
helpviewer_keywords: ["MI_Class_GetParentClassName","MI_Class_GetParentClassName function [Windows Management Infrastructure (MI)]","mi/MI_Class_GetParentClassName","wmi_v2.mi_class_getparentclassname"]
old-location: wmi_v2\mi_class_getparentclassname.htm
tech.root: wmi_v2
ms.assetid: a7e183f1-1136-46e0-a53d-39d06767e380
ms.date: 12/05/2018
ms.keywords: MI_Class_GetParentClassName, MI_Class_GetParentClassName function [Windows Management Infrastructure (MI)], mi/MI_Class_GetParentClassName, wmi_v2.mi_class_getparentclassname
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
 - MI_Class_GetParentClassName
 - mi/MI_Class_GetParentClassName
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
 - MI_Class_GetParentClassName
---

# MI_Class_GetParentClassName function


## -description

Gets the parent class name of the specified class.

## -parameters

### -param self [in]

A pointer to the class from which to retrieve the parent class name.

### -param name

A pointer to a pointer to the returned parent class name value. This string is owned by the class and does not need to be deleted. If there is no parent class, this will be <b>NULL</b>.

## -returns

This function returns MI_INLINE MI_Result.

