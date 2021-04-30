---
UID: NS:dwmapi._MilMatrix3x2D
title: MilMatrix3x2D (dwmapi.h)
description: Specifies a 3x2 matrix that describes a transform.
helpviewer_keywords: ["MIL_MATRIX3X2D","MilMatrix3x2D","MilMatrix3x2D structure [Desktop Window Manager]","_udwm_MilMatrix3x2D","_udwm_milmatrix3x2d_cpp","dwm.milmatrix3x2d","dwmapi/MilMatrix3x2D","winui._udwm_milmatrix3x2d"]
old-location: dwm\milmatrix3x2d.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\structures\milmatrix3x2d.htm
ms.date: 12/05/2018
ms.keywords: MIL_MATRIX3X2D, MilMatrix3x2D, MilMatrix3x2D structure [Desktop Window Manager], _udwm_MilMatrix3x2D, _udwm_milmatrix3x2d_cpp, dwm.milmatrix3x2d, dwmapi/MilMatrix3x2D, winui._udwm_milmatrix3x2d
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MilMatrix3x2D
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MilMatrix3x2D
 - dwmapi/_MilMatrix3x2D
 - MilMatrix3x2D
 - dwmapi/MilMatrix3x2D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dwmapi.h
api_name:
 - MilMatrix3x2D
---

# MilMatrix3x2D structure


## -description

Specifies a 3x2 matrix that describes a transform.

## -struct-fields

### -field S_11

The value at the (1,1) position of the matrix (first row, first column).

### -field S_12

The value at the (1,2) position of the matrix (first row, second column).

### -field S_21

The value at the (2,1) position of the matrix (second row, first column).

### -field S_22

The value at the (2,2) position of the matrix (second row, second column).

### -field DX

The value at the (3,1) position of the matrix (third row, first column).

### -field DY

The value at the (3,2) position of the matrix (third row, second column).

## -remarks

In Windows Vista, this structure was named MIL_MATRIX3X2D. It was renamed in Windows 7.

