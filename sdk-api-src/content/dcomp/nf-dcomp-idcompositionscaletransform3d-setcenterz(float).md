---
UID: NF:dcomp.IDCompositionScaleTransform3D.SetCenterZ(float)
title: IDCompositionScaleTransform3D::SetCenterZ(float)
author: windows-sdk-content
description: Changes the value of the CenterZ property of a 3D scale transform.
old-location: directcomp\idcompositionscaletransform3d_setcenterz_float.htm
tech.root: directcomp
ms.assetid: 69610037-28CD-49DA-8633-C26986AD17E7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDCompositionScaleTransform3D interface [DirectComposition],SetCenterZ method, IDCompositionScaleTransform3D.SetCenterZ, IDCompositionScaleTransform3D.SetCenterZ(float), IDCompositionScaleTransform3D::SetCenterZ, IDCompositionScaleTransform3D::SetCenterZ(float), SetCenterZ, SetCenterZ method [DirectComposition], SetCenterZ method [DirectComposition],IDCompositionScaleTransform3D interface, dcomp/IDCompositionScaleTransform3D::SetCenterZ, directcomp.idcompositionscaletransform3d_setcenterz_float
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
 - IDCompositionScaleTransform3D.SetCenterZ
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionScaleTransform3D::SetCenterZ(float)


## -description


Changes the value of the CenterZ property of a 3D scale transform.   The CenterZ property specifies the z-coordinate of the point about which scaling is performed. 


## -parameters




### -param centerZ [in]

Type: <b>float</b>

The new z-coordinate of the center point.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if the <i>centerZ</i> parameter is NaN, positive infinity, or negative infinity.



If the CenterZ property was previously animated, this method removes the animation and sets the CenterZ property to the specified static value.





## -see-also




<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform3D</a>



<a href="https://msdn.microsoft.com/959F8530-D2D5-46BC-9F29-F1DFC8029C12">IDCompositionScaleTransform3D::SetCenterX</a>



<a href="https://msdn.microsoft.com/C650032E-3344-4BE8-9018-F57EFECEBF61">IDCompositionScaleTransform3D::SetCenterY</a>
 

 

