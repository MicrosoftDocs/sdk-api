---
UID: NF:mi.MI_Class_GetMethodAt
title: MI_Class_GetMethodAt function (mi.h)
description: Gets details of a method based on the method index.
helpviewer_keywords: ["MI_Class_GetMethodAt","MI_Class_GetMethodAt function [Windows Management Infrastructure (MI)]","mi/MI_Class_GetMethodAt","wmi_v2.mi_class_getmethodat"]
old-location: wmi_v2\mi_class_getmethodat.htm
tech.root: wmi_v2
ms.assetid: 00239417-f771-48fa-afce-fef2ec99a171
ms.date: 12/05/2018
ms.keywords: MI_Class_GetMethodAt, MI_Class_GetMethodAt function [Windows Management Infrastructure (MI)], mi/MI_Class_GetMethodAt, wmi_v2.mi_class_getmethodat
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
 - MI_Class_GetMethodAt
 - mi/MI_Class_GetMethodAt
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
 - MI_Class_GetMethodAt
---

# MI_Class_GetMethodAt function


## -description

Gets details of a method based on the method index.

## -parameters

### -param self [in]

A pointer to the class object from which the method information is to be retrieved.

### -param index

Zero-based index of the requested method.

### -param name

A pointer to a pointer to the returned name of the method.  The memory associated with the name is valid until the class object is deleted. If this information is not needed, pass <b>NULL</b> for this parameter.

### -param qualifierSet [out, optional]

A pointer to a variable to receive the returned qualifier set. This parameter is optional. The memory associated with the qualifier set is valid until the class object is deleted. When you have finished using the class qualifier set, delete the class object by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a> function. If this information is not needed, pass <b>NULL</b> for this parameter.

### -param parameterSet [out, optional]

A pointer to a variable to receive the returned parameter set. The parameter set also contains the return type and return type qualifier set.   This parameter is optional. The memory associated with the parameter set is valid until the class object is deleted. When you have finished using the parameter set, delete the class object by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_class_delete">MI_Class_Delete</a> function. If this information is not needed, pass <b>NULL</b> for this parameter.

## -returns

This function returns MI_INLINE MI_Result.