---
UID: NS:dwrite.DWRITE_MATRIX
title: DWRITE_MATRIX (dwrite.h)
description: The DWRITE_MATRIX structure specifies the graphics transform to be applied to rendered glyphs.
helpviewer_keywords: ["DWRITE_MATRIX","DWRITE_MATRIX structure [Direct Write]","directwrite.dwrite_matrix","dwrite/DWRITE_MATRIX"]
old-location: directwrite\dwrite_matrix.htm
tech.root: DirectWrite
ms.assetid: fe4bd8ba-fc3b-4a04-8a72-9983d52f4404
ms.date: 12/05/2018
ms.keywords: DWRITE_MATRIX, DWRITE_MATRIX structure [Direct Write], directwrite.dwrite_matrix, dwrite/DWRITE_MATRIX
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - DWRITE_MATRIX
 - dwrite/DWRITE_MATRIX
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dwrite.h
api_name:
 - DWRITE_MATRIX
---

# DWRITE_MATRIX structure


## -description

The <b>DWRITE_MATRIX</b> structure specifies the graphics transform to be applied to rendered glyphs.

## -struct-fields

### -field m11

Type: <b>FLOAT</b>

A value indicating the horizontal scaling / cosine of rotation.

### -field m12

Type: <b>FLOAT</b>

A value indicating the vertical shear / sine of rotation.

### -field m21

Type: <b>FLOAT</b>

A value indicating the horizontal shear / negative sine of rotation.

### -field m22

Type: <b>FLOAT</b>

A value indicating the vertical scaling / cosine of rotation.

### -field dx

Type: <b>FLOAT</b>

A value indicating the horizontal shift (always orthogonal regardless of rotation).

### -field dy

Type: <b>FLOAT</b>

A value indicating the vertical shift (always orthogonal regardless of rotation.)

