---
UID: NF:dcomp.IDCompositionTranslateTransform3D.SetOffsetZ(float)
title: IDCompositionTranslateTransform3D::SetOffsetZ(float)
author: windows-sdk-content
description: Changes the value of the OffsetZ property of a 3D translation transform effect. The OffsetZ property specifies the distance to translate along the z-axis.
old-location: directcomp\idcompositiontranslatetransform3d_setoffsetz_float.htm
tech.root: directcomp
ms.assetid: 98FC07F4-BD13-448A-8421-9049CF9C0850
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDCompositionTranslateTransform3D interface [DirectComposition],SetOffsetZ method, IDCompositionTranslateTransform3D.SetOffsetZ, IDCompositionTranslateTransform3D.SetOffsetZ(float), IDCompositionTranslateTransform3D::SetOffsetZ, IDCompositionTranslateTransform3D::SetOffsetZ(float), SetOffsetZ, SetOffsetZ method [DirectComposition], SetOffsetZ method [DirectComposition],IDCompositionTranslateTransform3D interface, dcomp/IDCompositionTranslateTransform3D::SetOffsetZ, directcomp.idcompositiontranslatetransform3d_setoffsetz_float
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
 - IDCompositionTranslateTransform3D.SetOffsetZ
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
- IDCompositionTranslateTransform3D.SetOffsetZ
: 
---

# IDCompositionTranslateTransform3D::SetOffsetZ(float)


## -description


Changes the value of the OffsetZ property of a 3D translation transform effect. The OffsetZ property specifies the distance to translate along the z-axis.


## -parameters




### -param offsetZ [in]

Type: <b>float</b>

The distance to translate along the z-axis, in pixels.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>offsetZ</i> parameter is NaN, positive infinity, or negative infinity.



If the OffsetZ property was previously animated, this method removes the animation and sets the OffsetZ property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/C265E5FC-F7A1-4E87-8311-C4D0613DD7BC">IDCompositionTranslateTransform3D</a>



<a href="https://msdn.microsoft.com/61EDA0AA-0274-446E-9169-974AB84802FA">IDCompositionTranslateTransform3D::SetOffsetX</a>



<a href="https://msdn.microsoft.com/254DCA74-DB51-442D-9483-F7597643C538">IDCompositionTranslateTransform3D::SetOffsetY</a>
 

 

