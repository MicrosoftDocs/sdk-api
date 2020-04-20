---
UID: NE:dcomptypes.DCOMPOSITION_BACKFACE_VISIBILITY
title: DCOMPOSITION_BACKFACE_VISIBILITY (dcomptypes.h)
description: Specifies the backface visibility to be applied to a visual.helpviewer_keywords: ["DCOMPOSITION_BACKFACE_VISIBILITY","DCOMPOSITION_BACKFACE_VISIBILITY enumeration [DirectComposition]","DCOMPOSITION_BACKFACE_VISIBILITY_HIDDEN","DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT","DCOMPOSITION_BACKFACE_VISIBILITY_VISIBLE","dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY","dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY_HIDDEN","dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT","dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY_VISIBLE","directcomp.dcomposition_backface_visibility"]
old-location: directcomp\dcomposition_backface_visibility.htm
tech.root: directcomp
ms.assetid: F1FCB4E3-E29D-43AB-A438-CB21D0364F67
ms.date: 12/05/2018
ms.keywords: DCOMPOSITION_BACKFACE_VISIBILITY, DCOMPOSITION_BACKFACE_VISIBILITY enumeration [DirectComposition], DCOMPOSITION_BACKFACE_VISIBILITY_HIDDEN, DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT, DCOMPOSITION_BACKFACE_VISIBILITY_VISIBLE, dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY, dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY_HIDDEN, dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT, dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY_VISIBLE, directcomp.dcomposition_backface_visibility
f1_keywords:
- dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY
dev_langs:
- c++
req.header: dcomptypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
- DcompTypes.h
api_name:
- DCOMPOSITION_BACKFACE_VISIBILITY
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DCOMPOSITION_BACKFACE_VISIBILITY enumeration


## -description


Specifies the backface visibility to be applied to a visual.  


## -enum-fields




### -field DCOMPOSITION_BACKFACE_VISIBILITY_VISIBLE

Surfaces in this visual's sub-tree are visible regardless of transformation.


### -field DCOMPOSITION_BACKFACE_VISIBILITY_HIDDEN

Surfaces in this visual's sub-tree are only visible when facing the observer.


### -field DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT

The back face visibility is the same as that of the target visual's parent visual.


## -see-also




<a href="https://code.msdn.microsoft.com/windowsdesktop/DirectComposition-Backface-a2271f33">DirectComposition Backface and D2D Batching</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual2-setbackfacevisibility">IDCompositionVisual2::SetBackFaceVisibility</a>



<b>Sample</b>
 

 

