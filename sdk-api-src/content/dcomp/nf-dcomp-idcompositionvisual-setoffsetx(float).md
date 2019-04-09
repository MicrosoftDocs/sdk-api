---
UID: NF:dcomp.IDCompositionVisual.SetOffsetX(float)
title: IDCompositionVisual::SetOffsetX(float) (dcomp.h)
author: windows-sdk-content
description: Changes the value of the OffsetX property of this visual.
old-location: directcomp\idcompositionvisual_setoffsetx_float.htm
tech.root: directcomp
ms.assetid: 5A90D9F4-E28D-49D6-9E5A-511E9479BD97
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetOffsetX method, IDCompositionVisual.SetOffsetX, IDCompositionVisual.SetOffsetX(float), IDCompositionVisual::SetOffsetX, IDCompositionVisual::SetOffsetX(float), SetOffsetX, SetOffsetX method [DirectComposition], SetOffsetX method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetOffsetX, directcomp.idcompositionvisual_setoffsetx_float
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
 - IDCompositionVisual.SetOffsetX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual::SetOffsetX(float)


## -description


Changes the value of the OffsetX property of this visual.  The OffsetX property specifies the new offset of the visual along the x-axis, relative to the parent visual.


## -parameters




### -param offsetX [in]

Type: <b>float</b>

The new offset of the visual along the x-axis, in pixels.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>offsetX</i> parameter is NaN, positive infinity, or negative infinity.



Changing the OffsetX property of a visual transforms the coordinate system of the entire visual subtree that is rooted at that visual. If the Clip property of this visual is specified, the clip rectangle is also transformed.





A transformation that is specified by the Transform property is applied after the OffsetX property.  In other words, the effect of setting the Transform property and the OffsetX property is the same as setting only the Transform property on a transform group  object where the first member of the group is an <a href="https://msdn.microsoft.com/2215721e-a10d-4c9e-b5b7-1698afa547d8">IDCompositionTranslateTransform</a> object that has the same OffsetX value as <i>offsetX</i>. However, you should use  <b>IDCompositionVisual::SetOffsetX</b> whenever possible because it is slightly faster.

If the OffsetX and OffsetY properties are set to 0, and the Transform property is set to NULL, the coordinate system of the visual is the same as that of its parent.

If the OffsetX property was previously animated, this method removes the animation and sets the property to the specified static value.



#### Examples

For an example, see <a href="https://msdn.microsoft.com/86006C3C-67A8-4931-BE76-D0CA9DB19505">How to Build a Simple Visual Tree</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>



<a href="https://msdn.microsoft.com/E364BDB4-57E0-4206-9095-F39E6B5B9190">IDCompositionVisual::SetOffsetY</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

