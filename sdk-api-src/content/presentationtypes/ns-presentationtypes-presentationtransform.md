---
UID: NS:presentationtypes.PresentationTransform
tech.root: comp_swapchain
title: PresentationTransform
ms.date: 06/08/2021
targetos: Windows
description: Represents an arbitrary affine 2D transformation defined by a 3-by-2 matrix. (PresentationTransform)
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: presentationtypes.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: PresentationTransform
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - presentationtypes.h
api_name:
 - PresentationTransform
f1_keywords:
 - PresentationTransform
 - presentationtypes/PresentationTransform
dev_langs:
 - c++
---

## -description

Represents an arbitrary affine 2D transformation defined by a 3-by-2 matrix.

## -struct-fields

### -field M11

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The value of the first row and first column of this transform matrix structure.

### -field M12

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The value of the first row and second column of this transform matrix structure.

### -field M21

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The value of the second row and first column of this transform matrix structure.

### -field M22

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The value of the second row and second column of this transform matrix structure.

### -field M31

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The value of the third row and first column of this transform matrix structure.

### -field M32

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

The value of the third row and second column of this transform matrix structure.

## -remarks

## -see-also

