---
UID: NE:dcomptypes.DCOMPOSITION_BACKFACE_VISIBILITY
title: DCOMPOSITION_BACKFACE_VISIBILITY
author: windows-sdk-content
description: Specifies the backface visibility to be applied to a visual.
old-location: directcomp\dcomposition_backface_visibility.htm
tech.root: directcomp
ms.assetid: F1FCB4E3-E29D-43AB-A438-CB21D0364F67
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: DCOMPOSITION_BACKFACE_VISIBILITY, DCOMPOSITION_BACKFACE_VISIBILITY enumeration [DirectComposition], DCOMPOSITION_BACKFACE_VISIBILITY_HIDDEN, DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT, DCOMPOSITION_BACKFACE_VISIBILITY_VISIBLE, dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY, dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY_HIDDEN, dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY_INHERIT, dcomptypes/DCOMPOSITION_BACKFACE_VISIBILITY_VISIBLE, directcomp.dcomposition_backface_visibility
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="http://go.microsoft.com/fwlink/p/?linkid=313910">DirectComposition Backface and D2D Batching</a>



<a href="https://msdn.microsoft.com/A488A0B9-3CBE-477A-9688-84A7DA43D7F6">IDCompositionVisual2::SetBackFaceVisibility</a>



<b>Sample</b>
 

 

