---
UID: NF:dcomp.IDCompositionVisual3.SetTransform(IDCompositionTransform3D)
title: IDCompositionVisual3::SetTransform(IDCompositionTransform3D)
author: windows-sdk-content
description: Sets the Transform property of this visual to the specified 3D transform object.
old-location: directcomp\idcompositionvisual3_settransform_2.htm
tech.root: directcomp
ms.assetid: 04b20481-5d00-d8f9-290d-a8ab19ae6eba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDCompositionVisual3 interface [DirectComposition],SetTransform method, IDCompositionVisual3.SetTransform, IDCompositionVisual3.SetTransform(IDCompositionTransform3D), IDCompositionVisual3::SetTransform, IDCompositionVisual3::SetTransform(IDCompositionTransform3D), IDCompositionVisual3::SetTransform(IDCompositionTransform3D*), SetTransform, SetTransform method [DirectComposition], SetTransform method [DirectComposition],IDCompositionVisual3 interface, dcomp/IDCompositionVisual3::SetTransform, directcomp.idcompositionvisual3_settransform_2
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
 - IDCompositionVisual3.SetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual3::SetTransform(IDCompositionTransform3D)


## -description


Sets the Transform property of this visual to the specified 3D transform object.


## -parameters




### -param transform [in, optional]

Type: <b><a href="https://msdn.microsoft.com/81239AB4-C2A3-4E37-95E3-B3C10532EE15">IDCompositionTransform3D</a>*</b>

The transform object that is used to modify  the coordinate system of this visual. This parameter can point to 
            an <a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a> interface or one of its derived interfaces. This parameter can be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



Setting the Transform property transforms the coordinate system of the entire visual subtree that is rooted at this visual. If the Clip property of this visual is specified, the clip rectangle is also transformed.



If the Transform property previously specified a transform matrix, the newly specified transform object replaces the transform matrix.

A transformation specified by the Transform property is applied after the OffsetX and OffsetY properties. In other words, the effect of setting the Transform property and the OffsetX and OffsetY properties is the same as setting only the Transform property on a transform group where the first member of the group is an <a href="https://msdn.microsoft.com/en-us/library/Hh449113(v=VS.85).aspx">IDCompositionTranslateTransform</a> object that has those same OffsetX and OffsetY values. However, you should use the <a href="https://msdn.microsoft.com/en-us/library/Hh449161(v=VS.85).aspx">IDCompositionVisual::SetOffsetX</a> and <a href="https://msdn.microsoft.com/en-us/library/Hh449167(v=VS.85).aspx">SetOffsetY</a> methods whenever possible because they are slightly faster. 

This method fails if <i>transform</i> is an invalid pointer or if it was not created by the same <a href="https://msdn.microsoft.com/en-us/library/Hh437392(v=VS.85).aspx">IDCompositionDevice</a> interface that created this visual. The interface cannot be a custom implementation; only interfaces created by Microsoft DirectComposition can be used with this method.


If the <i>transform</i> parameter is NULL, the coordinate system of this visual is transformed only by its OffsetX and OffsetY properties. Setting the Transform property to NULL is equivalent to setting it to an <a href="https://msdn.microsoft.com/en-us/library/Hh437424(v=VS.85).aspx">IDCompositionMatrixTransform</a> object where the specified matrix is the identity matrix. However, an application should set the Transform property to NULL whenever possible because it is slightly faster.

If the OffsetX and OffsetY properties are set to 0, and the Transform property is set to NULL, the coordinate system of the visual is the same as that of its parent.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Hh437424(v=VS.85).aspx">IDCompositionMatrixTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh448924(v=VS.85).aspx">IDCompositionRotateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh448990(v=VS.85).aspx">IDCompositionScaleTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449057(v=VS.85).aspx">IDCompositionSkewTransform</a>



<a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449113(v=VS.85).aspx">IDCompositionTranslateTransform</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh449139(v=VS.85).aspx">IDCompositionVisual</a>



<a href="https://msdn.microsoft.com/en-us/library/Dn904490(v=VS.85).aspx">IDCompositionVisual3</a>



<a href="https://msdn.microsoft.com/0EFCDE12-3BF1-4D1F-8E28-54F3D7EEFFC1">IDCompositionVisual::SetOffsetX</a>



<a href="https://msdn.microsoft.com/E364BDB4-57E0-4206-9095-F39E6B5B9190">IDCompositionVisual::SetOffsetY</a>
 

 

