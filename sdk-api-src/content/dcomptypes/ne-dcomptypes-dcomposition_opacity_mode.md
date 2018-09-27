---
UID: NE:dcomptypes.DCOMPOSITION_OPACITY_MODE
title: DCOMPOSITION_OPACITY_MODE
author: windows-sdk-content
description: Specifies how the effective opacity value of a visual is applied to that visual’s content and children.
old-location: directcomp\dcomposition_opacity_mode.htm
tech.root: directcomp
ms.assetid: D768F699-39F6-4ED5-B3D7-D509871BCEAB
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DCOMPOSITION_OPACITY_MODE, DCOMPOSITION_OPACITY_MODE enumeration [DirectComposition], DCOMPOSITION_OPACITY_MODE_INHERIT, DCOMPOSITION_OPACITY_MODE_LAYER, DCOMPOSITION_OPACITY_MODE_MULTIPLY, dcomptypes/DCOMPOSITION_OPACITY_MODE, dcomptypes/DCOMPOSITION_OPACITY_MODE_INHERIT, dcomptypes/DCOMPOSITION_OPACITY_MODE_LAYER, dcomptypes/DCOMPOSITION_OPACITY_MODE_MULTIPLY, directcomp.dcomposition_opacity_mode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dcomptypes.h
api_name:
 - DCOMPOSITION_OPACITY_MODE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DCOMPOSITION_OPACITY_MODE enumeration


## -description


Specifies how the effective opacity value of a visual is applied to that visual’s content and children.


## -enum-fields




### -field DCOMPOSITION_OPACITY_MODE_LAYER

The target visual defines a logical layer into which its entire sub-tree is composed with a starting effective opacity of 1.0. The original opacity value is then used to blend the layer onto the visual’s background.


### -field DCOMPOSITION_OPACITY_MODE_MULTIPLY

The opacity value is multiplied with the effective opacity of the parent visual and the result is then individually applied to each piece of content in this visual’s sub-tree.


### -field DCOMPOSITION_OPACITY_MODE_INHERIT

The opacity mode is the same as that of the target visual’s parent visual.


## -see-also




<a href="https://msdn.microsoft.com/785DE91D-718B-4704-88E4-B8FB12586E5F">IDCompositionEffectGroup::SetOpacity</a>



IDCompositionVisual2::SetOpacityMode
 

 

