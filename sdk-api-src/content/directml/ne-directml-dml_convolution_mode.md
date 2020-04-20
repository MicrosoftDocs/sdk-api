---
UID: NE:directml.DML_CONVOLUTION_MODE
title: DML_CONVOLUTION_MODE
description: Defines constants that specify a mode for the DirectML convolution operator (as described by the DML_CONVOLUTION_OPERATOR_DESC structure).helpviewer_keywords: ["DML_CONVOLUTION_MODE","DML_CONVOLUTION_MODE enumeration","DML_CONVOLUTION_MODE_CONVOLUTION","DML_CONVOLUTION_MODE_CROSS_CORRELATION","direct3d12.dml_convolution_mode","directml/DML_CONVOLUTION_MODE","directml/DML_CONVOLUTION_MODE_CONVOLUTION","directml/DML_CONVOLUTION_MODE_CROSS_CORRELATION"]
old-location: direct3d12\dml_convolution_mode.htm
tech.root: direct3d12
ms.assetid: E3AA329D-1029-438C-A6F3-4720D5F5BE6C
ms.date: 12/5/2018
ms.keywords: DML_CONVOLUTION_MODE, DML_CONVOLUTION_MODE enumeration, DML_CONVOLUTION_MODE_CONVOLUTION, DML_CONVOLUTION_MODE_CROSS_CORRELATION, direct3d12.dml_convolution_mode, directml/DML_CONVOLUTION_MODE, directml/DML_CONVOLUTION_MODE_CONVOLUTION, directml/DML_CONVOLUTION_MODE_CROSS_CORRELATION
f1_keywords:
- directml/DML_CONVOLUTION_MODE
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_CONVOLUTION_MODE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_CONVOLUTION_MODE enumeration


## -description






Defines constants that specify a mode for the DirectML convolution operator (as described by the [DML_CONVOLUTION_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc) structure).


## -enum-fields




### -field DML_CONVOLUTION_MODE_CONVOLUTION

Specifies the convolution mode.


### -field DML_CONVOLUTION_MODE_CROSS_CORRELATION

Specifies the cross-correlation mode. If in doubt, use this mode—it is appropriate for the vast majority of machine learning (ML) models.


## -see-also




[DML_CONVOLUTION_OPERATOR_DESC](/windows/desktop/api/directml/ns-directml-dml_convolution_operator_desc)
 

 

