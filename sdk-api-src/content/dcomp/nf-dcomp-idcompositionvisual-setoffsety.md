---
UID: NF:dcomp.IDCompositionVisual.SetOffsetY
title: IDCompositionVisual::SetOffsetY
author: windows-sdk-content
description: Changes the value of the OffsetY property of this visual.
old-location: directcomp\idcompositionvisual_setoffsety_float.htm
tech.root: directcomp
ms.assetid: 7FF2433A-1741-4177-85C8-F5AE0D920EB4
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionVisual interface [DirectComposition],SetOffsetY method, IDCompositionVisual.SetOffsetY, IDCompositionVisual::SetOffsetY, IDCompositionVisual::SetOffsetY(float), SetOffsetY, SetOffsetY method [DirectComposition], SetOffsetY method [DirectComposition],IDCompositionVisual interface, dcomp/IDCompositionVisual::SetOffsetY, directcomp.idcompositionvisual_setoffsety_float
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
 - IDCompositionVisual.SetOffsetY
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual::SetOffsetY


## -description


Changes the value of the OffsetY property of this visual.  The OffsetY property specifies the new offset of the visual along the y-axis, relative to the parent visual.


## -parameters




### -param offsetY [in]

Type: <b>float</b>

The new offset of the visual along the y-axis, in pixels.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>offsetY</i> parameter is NaN, positive infinity, or negative infinity.



Changing the OffsetY property transforms the coordinate system of the entire visual subtree that is rooted at this visual. If the Clip property of this visual is specified, the clip rectangle is also transformed.



A transformation that is specified by the Transform property is applied after the OffsetY property.  In other words, the effect of setting the Transform property and the OffsetY property is the same as setting only the Transform property on a transform group object where the first member of the group is an <a href="https://msdn.microsoft.com/en-us/library/Hh449113(v=VS.85).aspx">IDCompositionTranslateTransform</a> object that has the same OffsetY value as <i>offsetY</i>. However, you should use  <b>IDCompositionVisual::SetOffsetY</b> whenever possible because it is slightly faster.

If the OffsetX and OffsetY properties are set to 0, and the Transform property is set to NULL, the coordinate system of the visual is the same as that of its parent.

If the OffsetY property was previously animated, this method removes the animation and sets the property to the specified static value.



#### Examples

For an example, see <a href="https://msdn.microsoft.com/86006C3C-67A8-4931-BE76-D0CA9DB19505">How to Build a Simple Visual Tree</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh449139(v=VS.85).aspx">IDCompositionVisual</a>



<a href="https://msdn.microsoft.com/0EFCDE12-3BF1-4D1F-8E28-54F3D7EEFFC1">IDCompositionVisual::SetOffsetX</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

