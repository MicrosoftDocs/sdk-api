---
UID: NF:mi.MI_ParameterSet_GetParameter
title: MI_ParameterSet_GetParameter function (mi.h)
description: Gets a method's parameter information based on a parameter name.
helpviewer_keywords: ["MI_ParameterSet_GetParameter","MI_ParameterSet_GetParameter function [Windows Management Infrastructure (MI)]","mi/MI_ParameterSet_GetParameter","wmi_v2.mi_parameterset_getparameter"]
old-location: wmi_v2\mi_parameterset_getparameter.htm
tech.root: wmi_v2
ms.assetid: ff895beb-8354-488d-9c97-2d0448da954a
ms.date: 12/05/2018
ms.keywords: MI_ParameterSet_GetParameter, MI_ParameterSet_GetParameter function [Windows Management Infrastructure (MI)], mi/MI_ParameterSet_GetParameter, wmi_v2.mi_parameterset_getparameter
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
 - MI_ParameterSet_GetParameter
 - mi/MI_ParameterSet_GetParameter
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
 - MI_ParameterSet_GetParameter
---

# MI_ParameterSet_GetParameter function


## -description

Gets a method's parameter information based on a parameter name.

## -parameters

### -param self [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_parameterset">MI_ParameterSet</a> structure.

### -param name [in]

Name of the parameter to get.

### -param parameterType [out]

Returned parameter type.

### -param referenceClass [out]

Returned reference class.

### -param qualifierSet [out]

Returned qualifier set of the parameter.

### -param index [out]

Returned zero-based index of the parameter.

## -returns

This function returns MI_INLINE MI_Result.