---
UID: NF:dcomp.IDCompositionDevice.CreateRotateTransform
title: IDCompositionDevice::CreateRotateTransform
author: windows-sdk-content
description: Creates a 2D rotation transform object.
old-location: directcomp\idcompositiondevice_createrotatetransform.htm
tech.root: directcomp
ms.assetid: 26a58b2c-1c68-4e38-963c-4df7512347f0
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateRotateTransform, CreateRotateTransform method [DirectComposition], CreateRotateTransform method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateRotateTransform method, IDCompositionDevice.CreateRotateTransform, IDCompositionDevice::CreateRotateTransform, dcomp/IDCompositionDevice::CreateRotateTransform, directcomp.idcompositiondevice_createrotatetransform
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
 - IDCompositionDevice.CreateRotateTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice::CreateRotateTransform


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




<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

