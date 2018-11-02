---
UID: NF:dcomp.IDCompositionDevice.CreateRotateTransform3D
title: IDCompositionDevice::CreateRotateTransform3D
author: windows-sdk-content
description: Creates a 3D rotation transform object.
old-location: directcomp\idcompositiondevice_createrotatetransform3d.htm
tech.root: directcomp
ms.assetid: 0F680BDB-F845-42AD-8888-B0E4A106D9CB
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateRotateTransform3D, CreateRotateTransform3D method [DirectComposition], CreateRotateTransform3D method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateRotateTransform3D method, IDCompositionDevice.CreateRotateTransform3D, IDCompositionDevice::CreateRotateTransform3D, dcomp/IDCompositionDevice::CreateRotateTransform3D, directcomp.idcompositiondevice_createrotatetransform3d
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
 - IDCompositionDevice.CreateRotateTransform3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice::CreateRotateTransform3D


## -description


Creates a 3D rotation transform object.


## -parameters




### -param rotateTransform3D [out]

Type: <b><a href="https://msdn.microsoft.com/BEC58B57-66A1-4645-A0B8-D546334E1E23">IDCompositionRotateTransform3D</a>**</b>

The new 3D rotation transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A new 3D rotation transform object has a default static value of zero for the Angle, CenterX, CenterY, AxisX, and AxisY properties, and a default static value of 1.0 for the AxisZ property.




## -see-also




<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionEffectGroup::SetTransform</a>



<a href="https://msdn.microsoft.com/CCA785F6-869C-460A-AF54-573BDE798685">IDCompositionVisual::SetEffect</a>
 

 

