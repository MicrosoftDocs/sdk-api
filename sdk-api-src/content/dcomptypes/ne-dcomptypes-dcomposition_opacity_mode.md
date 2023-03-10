---
UID: NE:dcomptypes.DCOMPOSITION_OPACITY_MODE
title: DCOMPOSITION_OPACITY_MODE (dcomptypes.h)
description: Specifies how the effective opacity value of a visual is applied to that visual’s content and children.
helpviewer_keywords: ["DCOMPOSITION_OPACITY_MODE","DCOMPOSITION_OPACITY_MODE enumeration [DirectComposition]","DCOMPOSITION_OPACITY_MODE_INHERIT","DCOMPOSITION_OPACITY_MODE_LAYER","DCOMPOSITION_OPACITY_MODE_MULTIPLY","dcomptypes/DCOMPOSITION_OPACITY_MODE","dcomptypes/DCOMPOSITION_OPACITY_MODE_INHERIT","dcomptypes/DCOMPOSITION_OPACITY_MODE_LAYER","dcomptypes/DCOMPOSITION_OPACITY_MODE_MULTIPLY","directcomp.dcomposition_opacity_mode"]
old-location: directcomp\dcomposition_opacity_mode.htm
tech.root: directcomp
ms.assetid: D768F699-39F6-4ED5-B3D7-D509871BCEAB
ms.date: 12/05/2018
ms.keywords: DCOMPOSITION_OPACITY_MODE, DCOMPOSITION_OPACITY_MODE enumeration [DirectComposition], DCOMPOSITION_OPACITY_MODE_INHERIT, DCOMPOSITION_OPACITY_MODE_LAYER, DCOMPOSITION_OPACITY_MODE_MULTIPLY, dcomptypes/DCOMPOSITION_OPACITY_MODE, dcomptypes/DCOMPOSITION_OPACITY_MODE_INHERIT, dcomptypes/DCOMPOSITION_OPACITY_MODE_LAYER, dcomptypes/DCOMPOSITION_OPACITY_MODE_MULTIPLY, directcomp.dcomposition_opacity_mode
req.header: dcomptypes.h
req.include-header: DComp.h
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
 - DCOMPOSITION_OPACITY_MODE
 - dcomptypes/DCOMPOSITION_OPACITY_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dcomptypes.h
api_name:
 - DCOMPOSITION_OPACITY_MODE
---

# DCOMPOSITION_OPACITY_MODE enumeration


## -description

Specifies how the effective opacity value of a visual is applied to that visual’s content and children.

## -enum-fields

### -field DCOMPOSITION_OPACITY_MODE_LAYER:0

The target visual defines a logical layer into which its entire sub-tree is composed with a starting effective opacity of 1.0. The original opacity value is then used to blend the layer onto the visual’s background.

### -field DCOMPOSITION_OPACITY_MODE_MULTIPLY:1

The opacity value is multiplied with the effective opacity of the parent visual and the result is then individually applied to each piece of content in this visual’s sub-tree.

### -field DCOMPOSITION_OPACITY_MODE_INHERIT:0xffffffff

The opacity mode is the same as that of the target visual’s parent visual.

## -see-also

<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositioneffectgroup-setopacity(float)">IDCompositionEffectGroup::SetOpacity</a>



IDCompositionVisual2::SetOpacityMode

