---
UID: NS:dwrite.DWRITE_INLINE_OBJECT_METRICS
title: DWRITE_INLINE_OBJECT_METRICS (dwrite.h)
description: Contains properties describing the geometric measurement of an application-defined inline object.
helpviewer_keywords: ["DWRITE_INLINE_OBJECT_METRICS","DWRITE_INLINE_OBJECT_METRICS structure [Direct Write]","directwrite.dwrite_inline_object_metrics","dwrite/DWRITE_INLINE_OBJECT_METRICS"]
old-location: directwrite\dwrite_inline_object_metrics.htm
tech.root: DirectWrite
ms.assetid: a42d612c-3d16-4c27-a1d8-1cfb9de2f8b1
ms.date: 12/05/2018
ms.keywords: DWRITE_INLINE_OBJECT_METRICS, DWRITE_INLINE_OBJECT_METRICS structure [Direct Write], directwrite.dwrite_inline_object_metrics, dwrite/DWRITE_INLINE_OBJECT_METRICS
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
 - DWRITE_INLINE_OBJECT_METRICS
 - dwrite/DWRITE_INLINE_OBJECT_METRICS
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
 - DWRITE_INLINE_OBJECT_METRICS
---

# DWRITE_INLINE_OBJECT_METRICS structure


## -description

Contains properties describing the geometric measurement of an
application-defined inline object.

## -struct-fields

### -field width

Type: <b>FLOAT</b>

The width of the inline object.

### -field height

Type: <b>FLOAT</b>

The height of the inline object.

### -field baseline

Type: <b>FLOAT</b>

The distance from the top of the object to the point where it is lined up with the adjacent text. 
     If the baseline is at the bottom, then <b>baseline</b> simply equals <b>height</b>.

### -field supportsSideways

Type: <b>BOOL</b>

A Boolean flag that indicates whether the object is to be placed upright or alongside the text baseline for vertical text.

