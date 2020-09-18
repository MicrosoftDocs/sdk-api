---
UID: NF:mi.MI_ParameterSet_GetParameterCount
title: MI_ParameterSet_GetParameterCount function (mi.h)
description: Gets the number of parameters in a method's parameter set.
helpviewer_keywords: ["MI_ParameterSet_GetParameterCount","MI_ParameterSet_GetParameterCount function [Windows Management Infrastructure (MI)]","mi/MI_ParameterSet_GetParameterCount","wmi_v2.mi_parameterset_getparametercount"]
old-location: wmi_v2\mi_parameterset_getparametercount.htm
tech.root: wmi_v2
ms.assetid: 4b1ca06f-426c-483f-a571-b49eb06991e1
ms.date: 12/05/2018
ms.keywords: MI_ParameterSet_GetParameterCount, MI_ParameterSet_GetParameterCount function [Windows Management Infrastructure (MI)], mi/MI_ParameterSet_GetParameterCount, wmi_v2.mi_parameterset_getparametercount
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
 - MI_ParameterSet_GetParameterCount
 - mi/MI_ParameterSet_GetParameterCount
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
 - MI_ParameterSet_GetParameterCount
---

# MI_ParameterSet_GetParameterCount function


## -description

Gets the number of parameters in a method's parameter set.

## -parameters

### -param self [in]

<a href="/windows/desktop/api/mi/ns-mi-mi_parameterset">MI_ParameterSet</a> structure.

### -param count [out]

Returned number of parameters.

## -returns

This function returns MI_INLINE MI_Result.