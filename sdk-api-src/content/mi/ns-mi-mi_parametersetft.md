---
UID: NS:mi._MI_ParameterSetFT
title: MI_ParameterSetFT (mi.h)
description: A support structure used in the MI_ParameterSet structure. Use the functions with the name prefix MI_ParameterSet_ to manipulate these structures.
helpviewer_keywords: ["MI_ParameterSetFT","MI_ParameterSetFT structure [Windows Management Infrastructure (MI)]","mi/MI_ParameterSetFT","wmi_v2.mi_parametersetft"]
old-location: wmi_v2\mi_parametersetft.htm
tech.root: wmi_v2
ms.assetid: 48e10e9c-8e50-4811-bd2a-1934d27373f0
ms.date: 12/05/2018
ms.keywords: MI_ParameterSetFT, MI_ParameterSetFT structure [Windows Management Infrastructure (MI)], mi/MI_ParameterSetFT, wmi_v2.mi_parametersetft
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
req.typenames: MI_ParameterSetFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_ParameterSetFT
 - mi/_MI_ParameterSetFT
 - MI_ParameterSetFT
 - mi/MI_ParameterSetFT
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
 - MI_ParameterSetFT
---

## -description

A support structure used in the <a href="/windows/desktop/api/mi/ns-mi-mi_parameterset">MI_ParameterSet</a> structure.  Use the functions with the name prefix MI_ParameterSet_ to manipulate these structures.

## -struct-fields

### -field GetMethodReturnType

Gets the method return type and qualifier set for a specified parameter set. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_parameterset_getmethodreturntype">MI_ParameterSet_GetMethodReturnType</a>.

### -field GetParameter

Gets a method's parameter information based on a parameter name. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_parameterset_getparameter">MI_ParameterSet_GetParameter</a>.

### -field GetParameterAt

Gets a method's parameter information at the specified index. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_parameterset_getparameterat">MI_ParameterSet_GetParameterAt</a>.

### -field GetParameterCount

Gets the number of parameters in a parameter set. See <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_parameterset_getparametercount">MI_ParameterSet_GetParameterCount</a>.
