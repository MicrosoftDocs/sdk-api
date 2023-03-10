---
UID: NF:mi.MI_ParameterSet_GetMethodReturnType
title: MI_ParameterSet_GetMethodReturnType function (mi.h)
description: Gets the method return type and qualifier set for a specified parameter set.
helpviewer_keywords: ["MI_ParameterSet_GetMethodReturnType","MI_ParameterSet_GetMethodReturnType function [Windows Management Infrastructure (MI)]","mi/MI_ParameterSet_GetMethodReturnType","wmi_v2.mi_parameterset_getmethodreturntype"]
old-location: wmi_v2\mi_parameterset_getmethodreturntype.htm
tech.root: wmi_v2
ms.assetid: 8d2e881a-72a8-4819-a407-b7381ab7a94a
ms.date: 12/05/2018
ms.keywords: MI_ParameterSet_GetMethodReturnType, MI_ParameterSet_GetMethodReturnType function [Windows Management Infrastructure (MI)], mi/MI_ParameterSet_GetMethodReturnType, wmi_v2.mi_parameterset_getmethodreturntype
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
 - MI_ParameterSet_GetMethodReturnType
 - mi/MI_ParameterSet_GetMethodReturnType
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
 - MI_ParameterSet_GetMethodReturnType
---

# MI_ParameterSet_GetMethodReturnType function


## -description

Gets the method return type and qualifier set for a specified parameter set.

## -parameters

### -param self [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_parameterset">MI_ParameterSet</a> structure.

### -param returnType [out]

Returned method return type.

### -param qualifierSet [out]

The returned qualifier set for the method name and return type.

## -returns

This function returns MI_INLINE MI_Result.