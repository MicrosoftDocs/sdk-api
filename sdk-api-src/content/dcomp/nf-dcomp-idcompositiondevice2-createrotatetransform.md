---
UID: NF:dcomp.IDCompositionDevice2.CreateRotateTransform
title: IDCompositionDevice2::CreateRotateTransform (dcomp.h)
author: windows-sdk-content
description: Creates a 2D rotation transform object.
old-location: directcomp\idcompositiondevice2_createrotatetransform.htm
tech.root: directcomp
ms.assetid: C4F0187C-FB3C-447A-AD1E-5094004273F5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateRotateTransform, CreateRotateTransform method [DirectComposition], CreateRotateTransform method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateRotateTransform method, IDCompositionDevice2.CreateRotateTransform, IDCompositionDevice2::CreateRotateTransform, dcomp/IDCompositionDevice2::CreateRotateTransform, directcomp.idcompositiondevice2_createrotatetransform
ms.topic: method
req.header: dcomp.h
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
 - IDCompositionDevice2.CreateRotateTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDCompositionDevice2::CreateRotateTransform


## -description


Creates a 2D rotation transform object.


## -parameters




### -param rotateTransform [out]

Type: <b><a href="https://msdn.microsoft.com/6c92bd6b-4479-45c2-986c-0a6c91248361">IDCompositionRotateTransform</a>**</b>

The new rotation transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A new 2D rotation transform object has a static value of zero for the Angle, CenterX, and CenterY properties.




## -see-also




<a href="https://msdn.microsoft.com/0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0">IDCompositionDevice2</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

