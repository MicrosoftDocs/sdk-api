---
UID: NS:directml.DML_SCALE_BIAS
title: DML_SCALE_BIAS
description: Contains the values of scale and bias terms supplied to a DirectML operator. Scale and bias have the effect of applying the function g(x) = x * Scale + Bias.
helpviewer_keywords: ["DML_SCALE_BIAS","DML_SCALE_BIAS structure","direct3d12.dml_scale_bias","directml/DML_SCALE_BIAS"]
old-location: direct3d12\dml_scale_bias.htm
tech.root: directml
ms.assetid: 56E5BD59-DD7C-40FF-8B85-BD405FDE8E29
ms.date: 12/5/2018
ms.keywords: DML_SCALE_BIAS, DML_SCALE_BIAS structure, direct3d12.dml_scale_bias, directml/DML_SCALE_BIAS
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DML_SCALE_BIAS
 - directml/DML_SCALE_BIAS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_SCALE_BIAS
---

## -description

Contains the values of scale and bias terms supplied to a DirectML operator. Scale and bias have the effect of applying the function g(x) = x * <i>Scale</i> + <i>Bias</i>.

## -struct-fields

### -field Scale

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The scale term in g(x) = x * <i>Scale</i> + <i>Bias</i>.

### -field Bias

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The bias term in g(x) = x * <i>Scale</i> + <i>Bias</i>.
