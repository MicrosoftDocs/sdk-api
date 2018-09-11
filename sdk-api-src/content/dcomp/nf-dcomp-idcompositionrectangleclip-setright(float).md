---
UID: NF:dcomp.IDCompositionRectangleClip.SetRight(float)
title: IDCompositionRectangleClip::SetRight(float)
author: windows-sdk-content
description: Changes the value of the Right property of a clip rectangle.
old-location: directcomp\idcompositionrectangleclip_setright_float.htm
tech.root: directcomp
ms.assetid: FB27BB00-239A-42A8-86D3-C78E2E8E820B
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDCompositionRectangleClip interface [DirectComposition],SetRight method, IDCompositionRectangleClip.SetRight, IDCompositionRectangleClip.SetRight(float), IDCompositionRectangleClip::SetRight, IDCompositionRectangleClip::SetRight(float), SetRight, SetRight method [DirectComposition], SetRight method [DirectComposition],IDCompositionRectangleClip interface, dcomp/IDCompositionRectangleClip::SetRight, directcomp.idcompositionrectangleclip_setright_float
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
 - IDCompositionRectangleClip.SetRight
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionRectangleClip::SetRight(float)


## -description


Changes the value of the Right property of a clip rectangle. The Right property specifies the x-coordinate of the lower-right corner of the clip rectangle.
      


## -parameters




### -param right [in]

Type: <b>float</b>

The new value of the Right property, in pixels. This parameter has a numerical limit of -2^21 to 2^21. 
            The API accepts numbers outside of this range, but they are always clamped to this range.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.
            




## -remarks



This method fails if the <i>right</i> parameter is NaN, positive infinity, or negative infinity.

      

If the Right property was previously animated, this method removes the animation and sets the Right property to the specified static value.
      




## -see-also




<a href="https://msdn.microsoft.com/486bcdb9-e353-4ca2-b24c-af863dda7470">IDCompositionRectangleClip</a>
 

 

