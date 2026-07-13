---
UID: NS:interactioncontext.MANIPULATION_TRANSFORM
title: MANIPULATION_TRANSFORM (interactioncontext.h)
description: Defines the transformation data for a manipulation.
helpviewer_keywords: ["MANIPULATION_TRANSFORM","MANIPULATION_TRANSFORM structure","input_intcontext.manipulation_transform","interactioncontext.manipulation_transform","interactioncontext/MANIPULATION_TRANSFORM"]
old-location: input_intcontext\manipulation_transform.htm
tech.root: input_intcontext
ms.assetid: f1019207-3197-4ccc-a795-01b868dcc9ca
ms.date: 12/05/2018
ms.keywords: MANIPULATION_TRANSFORM, MANIPULATION_TRANSFORM structure, input_intcontext.manipulation_transform, interactioncontext.manipulation_transform, interactioncontext/MANIPULATION_TRANSFORM
req.header: interactioncontext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: MANIPULATION_TRANSFORM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MANIPULATION_TRANSFORM
 - interactioncontext/MANIPULATION_TRANSFORM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - interactioncontext.h
api_name:
 - MANIPULATION_TRANSFORM
---

# MANIPULATION_TRANSFORM structure

## -description

Defines the transformation data for a manipulation.

## -struct-fields

### -field translationX

Translation along the x-axis, in HIMETRIC units.

### -field translationY

Translation along the y-axis, in HIMETRIC units.

### -field scale

Change in scale as a percentage, in HIMETRIC units.

### -field expansion

Expansion in user-defined coordinates, in HIMETRIC units.

### -field rotation

Change in rotation, in radians.

## -see-also
