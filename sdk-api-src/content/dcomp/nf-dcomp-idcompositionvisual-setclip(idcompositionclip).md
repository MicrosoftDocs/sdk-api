---
UID: NF:dcomp.IDCompositionVisual.SetClip(IDCompositionClip)
title: IDCompositionVisual::SetClip(IDCompositionClip)
author: windows-sdk-content
description: Sets the Clip property of this visual to the specified clip object.
old-location: directcomp\idcompositionvisual_setclip_idcompositionclip.htm
tech.root: directcomp
ms.assetid: 504938a1-2775-477d-a077-7afc4e333f36
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetClip method, IDCompositionVisual.SetClip, IDCompositionVisual.SetClip(IDCompositionClip), IDCompositionVisual::SetClip, IDCompositionVisual::SetClip(IDCompositionClip), IDCompositionVisual::SetClip(IDCompositionClip*), SetClip, SetClip method [DirectComposition], SetClip method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetClip, directcomp.idcompositionvisual_setclip_idcompositionclip
ms.topic: method
req.header: dcomp.h
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
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionVisual.SetClip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual::SetClip(IDCompositionClip)


## -description


Sets the Clip property of this visual to the specified clip object. The Clip property restricts the rendering of the visual subtree 
        that is rooted at this visual to a rectangular region.
      


## -parameters




### -param clip [in, optional]

Type: <b><a href="https://msdn.microsoft.com/647638f4-7eca-42bc-a083-3d9d15089648">IDCompositionClip</a>*</b>

The clip object to associate with this visual. This parameter can be NULL.  All float properties of IDCompositionRectangleClip have a numerical limit of -2^21 to 2^21.
              The API accepts numbers outside of this range, but they are always clamped to this range.
            


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. 
              See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.
            




## -remarks



Setting the Clip property clips this visual along with all visuals in the subtree that is rooted at this visual. The clip is transformed by the OffsetX, OffsetY,  and Transform properties.

If the Clip property previously specified a clip rectangle, the newly specified Clip object replaces the clip rectangle.

This method fails if <i>clip</i> is an invalid pointer or if it was not created by the 
        same <a href="https://msdn.microsoft.com/en-us/library/Hh437392(v=VS.85).aspx">IDCompositionDevice</a> interface that created this visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.
      

If <i>clip</i> is NULL, the visual is not clipped relative to its parent. However, the visual is clipped by the clip object of the parent visual, 
        or by the closest ancestor visual that has a clip object. Setting <i>clip</i> to NULL is similar to specifying a clip object whose 
        clip rectangle has the left and top sides set to negative infinity, and the right and bottom sides set to positive infinity. Using a NULL clip object results in slightly better performance.
      

If <i>clip</i> specifies a clip object that has an empty rectangle, the visual is fully clipped; that is, the visual is included in the visual tree, 
        but it does not render anything. To exclude a particular visual from a composition, remove the visual from the visual tree instead of setting an empty clip rectangle. 
        Removing the visual results in better performance.
      




## -see-also




<a href="https://msdn.microsoft.com/B6E0D8F5-B6B9-40CC-B079-850AC8F2D538">Clipping</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh437434(v=VS.85).aspx">IDCompositionRectangleClip</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449139(v=VS.85).aspx">IDCompositionVisual</a>
 

 

