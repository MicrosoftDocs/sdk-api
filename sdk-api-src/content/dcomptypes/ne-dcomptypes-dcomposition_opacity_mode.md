---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 

