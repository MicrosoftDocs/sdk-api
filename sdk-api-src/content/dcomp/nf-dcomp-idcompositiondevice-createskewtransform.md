---
UID: NF:dcomp.IDCompositionDevice.CreateSkewTransform
title: IDCompositionDevice::CreateSkewTransform
author: windows-sdk-content
description: Creates a 2D skew transform object.
old-location: directcomp\idcompositiondevice_createskewtransform.htm
tech.root: directcomp
ms.assetid: c67d1c75-8704-44b3-8794-58cf08ea2572
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateSkewTransform, CreateSkewTransform method [DirectComposition], CreateSkewTransform method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateSkewTransform method, IDCompositionDevice.CreateSkewTransform, IDCompositionDevice::CreateSkewTransform, dcomp/IDCompositionDevice::CreateSkewTransform, directcomp.idcompositiondevice_createskewtransform
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
 - IDCompositionDevice.CreateSkewTransform
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
- IDCompositionDevice.CreateSkewTransform
: 
---

# IDCompositionDevice::CreateSkewTransform


## -description


Creates a 2D skew transform object.


## -parameters




### -param skewTransform [out]

Type: <b><a href="https://msdn.microsoft.com/c1dbc11f-b8e3-487e-84f0-517ebaf65de8">IDCompositionSkewTransform</a>**</b>

The new 2D skew transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A new 2D skew transform object has a static value of zero for the AngleX, AngleY, CenterX, and CenterY properties.




## -see-also




<a href="https://msdn.microsoft.com/081a14ed-c152-4e0a-b85b-1111d825ce53">IDCompositionDevice</a>



<a href="https://msdn.microsoft.com/DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D">IDCompositionVisual::SetTransform</a>
 

 

