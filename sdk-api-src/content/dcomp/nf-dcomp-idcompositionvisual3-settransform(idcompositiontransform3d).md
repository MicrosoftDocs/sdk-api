---
UID: NF:dcomp.IDCompositionVisual3.SetTransform(IDCompositionTransform3D)
title: IDCompositionVisual3::SetTransform(IDCompositionTransform3D)
author: windows-sdk-content
description: Sets the Transform property of this visual to the specified 4-by-4 transform matrix.
old-location: directcomp\idcompositionvisual3_settransform_1.htm
tech.root: directcomp
ms.assetid: 1deb9c84-1a5b-5dac-af0f-ae6b49a9c473
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IDCompositionVisual3 interface [DirectComposition],SetTransform method, IDCompositionVisual3.SetTransform, IDCompositionVisual3.SetTransform(IDCompositionTransform3D), IDCompositionVisual3::SetTransform, IDCompositionVisual3::SetTransform(IDCompositionTransform3D), IDCompositionVisual3::SetTransform(const D2D_MATRIX_4X4_F&), SetTransform, SetTransform method [DirectComposition], SetTransform method [DirectComposition],IDCompositionVisual3 interface, dcomp/IDCompositionVisual3::SetTransform, directcomp.idcompositionvisual3_settransform_1
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
 - IDCompositionVisual3.SetTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionVisual3::SetTransform(IDCompositionTransform3D)


## -description


Sets the Transform property of this visual to the specified 4-by-4 transform matrix.  


## -parameters




### -param transform

TBD




#### - matrix [in, ref]

Type: <b>const <a href="https://msdn.microsoft.com/c8a54bad-4376-479b-8529-1e407623e473">D2D_MATRIX_4X4_F</a></b>

The 4-by-4 transform matrix that is used to modify  the coordinate system of this visual.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



Setting the Transform property transforms the coordinate system of the entire visual subtree that is rooted at this visual. If the Clip property of this visual is specified, the clip rectangle is also transformed.



If the Transform property previously specified a transform object, the newly specified transform matrix replaces the transform object.




## -see-also




<a href="https://msdn.microsoft.com/150e33f2-3d76-44a8-b2fe-5a2b4a532c3c">IDCompositionMatrixTransform</a>



<a href="https://msdn.microsoft.com/6c92bd6b-4479-45c2-986c-0a6c91248361">IDCompositionRotateTransform</a>



<a href="https://msdn.microsoft.com/8e59c484-b7c5-446a-a5d6-e00371e2c08a">IDCompositionScaleTransform</a>



<a href="https://msdn.microsoft.com/c1dbc11f-b8e3-487e-84f0-517ebaf65de8">IDCompositionSkewTransform</a>



<a href="https://msdn.microsoft.com/22f0d199-5162-4869-909e-d0ed0059b773">IDCompositionTransform</a>



<a href="https://msdn.microsoft.com/2215721e-a10d-4c9e-b5b7-1698afa547d8">IDCompositionTranslateTransform</a>



<a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>



<a href="https://msdn.microsoft.com/c7bf4e6f-119b-2122-1103-d6ab240121c9">IDCompositionVisual3</a>



<a href="https://msdn.microsoft.com/0EFCDE12-3BF1-4D1F-8E28-54F3D7EEFFC1">IDCompositionVisual::SetOffsetX</a>



<a href="https://msdn.microsoft.com/E364BDB4-57E0-4206-9095-F39E6B5B9190">IDCompositionVisual::SetOffsetY</a>
 

 

