---
UID: NF:mi.MI_Class_GetNameSpace
title: MI_Class_GetNameSpace function (mi.h)
description: Gets the namespace name of the specified class.
helpviewer_keywords: ["MI_Class_GetNameSpace","MI_Class_GetNameSpace function [Windows Management Infrastructure (MI)]","mi/MI_Class_GetNameSpace","wmi_v2.mi_class_getnamespace"]
old-location: wmi_v2\mi_class_getnamespace.htm
tech.root: wmi_v2
ms.assetid: 64ee42d6-d6ad-4a41-83f4-48de191a853c
ms.date: 12/05/2018
ms.keywords: MI_Class_GetNameSpace, MI_Class_GetNameSpace function [Windows Management Infrastructure (MI)], mi/MI_Class_GetNameSpace, wmi_v2.mi_class_getnamespace
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
 - MI_Class_GetNameSpace
 - mi/MI_Class_GetNameSpace
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
 - MI_Class_GetNameSpace
---

# MI_Class_GetNameSpace function


## -description

Gets the namespace name of the specified class.

## -parameters

### -param self [in]

A pointer to the class from which to get the namespace name.

### -param nameSpace

A pointer to a pointer to the returned namespace name value. This string is owned by the class and does not need to be deleted.

## -returns

This function returns MI_INLINE MI_Result.

