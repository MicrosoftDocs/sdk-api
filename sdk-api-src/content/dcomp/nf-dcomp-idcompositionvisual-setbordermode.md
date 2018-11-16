---
UID: NF:dcomp.IDCompositionVisual.SetBorderMode
title: IDCompositionVisual::SetBorderMode
author: windows-sdk-content
description: Sets the BorderMode property, which specifies how to compose the edges of bitmaps and clips associated with this visual, or with visuals in the subtree rooted at this visual.
old-location: directcomp\idcompositionvisual_setbordermode.htm
tech.root: directcomp
ms.assetid: 88C77869-B08D-43F6-8A1E-A112743C0404
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetBorderMode method, IDCompositionVisual.SetBorderMode, IDCompositionVisual::SetBorderMode, SetBorderMode, SetBorderMode method [DirectComposition], SetBorderMode method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetBorderMode, directcomp.idcompositionvisual_setbordermode
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDCompositionVisual.SetBorderMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dcomp.h
: 
- IDCompositionVisual.SetBorderMode
: 
---

# IDCompositionVisual::SetBorderMode


## -description


Sets the BorderMode property, which specifies how to compose the edges of bitmaps and clips associated with this visual, or with visuals in the subtree rooted at this visual.


## -parameters




### -param borderMode [in]

Type: <b><a href="https://msdn.microsoft.com/26CDDC8A-27F5-4BE4-B345-70FF66ED5C9A">DCOMPOSITION_BORDER_MODE</a></b>

The border mode to use.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



The border mode affects how the edges of a bitmap are composed when the bitmap is transformed such that the edges are not exactly axis-aligned and at precise pixel boundaries. It also affects how content is clipped at the corners of a clip that has rounded corners, and at the edge of a clip that is transformed such that the edges are not exactly axis-aligned and at precise pixel boundaries.



By default, a visual inherits the border mode of  its parent visual, which may inherit the border mode of its parent visual, and so on. A visual uses the default border mode if this method is never called for the visual, or if this method is called with <a href="dcomposition_border_mode.htm">DCOMPOSITION_BORDER_MODE_INHERIT</a>. If no visuals set the border mode, the default for the entire visual tree is aliased rendering, which offers the lowest visual quality but the highest performance.



If the <i>borderMode</i> parameter is anything other than <a href="dcomposition_border_mode.htm">DCOMPOSITION_BORDER_MODE_INHERIT</a>, this visual's bitmap and clip are composed with the specified border mode. In addition, this border mode becomes the new default for the children of the current visual. That is, if the border mode of this visual's children is unchanged or explicitly set to <b>DCOMPOSITION_BORDER_MODE_INHERIT</b>, the bitmaps and clips of the child visuals are composed using the border mode of this visual.





## -see-also




<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>
 

 

