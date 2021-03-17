---
UID: NF:mi.MI_Class_GetClassName
title: MI_Class_GetClassName function (mi.h)
description: Gets the class name of the specified class.
helpviewer_keywords: ["MI_Class_GetClassName","MI_Class_GetClassName function [Windows Management Infrastructure (MI)]","mi/MI_Class_GetClassName","wmi_v2.mi_class_getclassname"]
old-location: wmi_v2\mi_class_getclassname.htm
tech.root: wmi_v2
ms.assetid: 405639e7-74b0-4cda-9883-f8442976200a
ms.date: 12/05/2018
ms.keywords: MI_Class_GetClassName, MI_Class_GetClassName function [Windows Management Infrastructure (MI)], mi/MI_Class_GetClassName, wmi_v2.mi_class_getclassname
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
 - MI_Class_GetClassName
 - mi/MI_Class_GetClassName
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
 - MI_Class_GetClassName
---

# MI_Class_GetClassName function


## -description

Gets the class name of the specified class.

## -parameters

### -param self [in]

A pointer to a class from which to get the name.

### -param className

A pointer to a pointer to a returned class name value. This string is borrowed from the class object; the caller must not delete the string.

## -returns

This function returns MI_INLINE MI_Result.

