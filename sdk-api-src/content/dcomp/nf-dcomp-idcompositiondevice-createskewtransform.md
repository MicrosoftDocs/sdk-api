---
UID: NF:dcomp.IDCompositionDevice.CreateSkewTransform
title: IDCompositionDevice::CreateSkewTransform (dcomp.h)
author: windows-sdk-content
description: Creates a 2D skew transform object.
old-location: directcomp\idcompositiondevice_createskewtransform.htm
tech.root: directcomp
ms.assetid: c67d1c75-8704-44b3-8794-58cf08ea2572
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateSkewTransform, CreateSkewTransform method [DirectComposition], CreateSkewTransform method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],CreateSkewTransform method, IDCompositionDevice.CreateSkewTransform, IDCompositionDevice::CreateSkewTransform, dcomp/IDCompositionDevice::CreateSkewTransform, directcomp.idcompositiondevice_createskewtransform
ms.topic: method
f1_keywords: 
 - "dcomp/IDCompositionDevice.CreateSkewTransform"
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
ms.custom: 19H1
---

# IDCompositionDevice::CreateSkewTransform


## -description


Creates a 2D skew transform object.


## -parameters




### -param skewTransform [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositionskewtransform">IDCompositionSkewTransform</a>**</b>

The new 2D skew transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://docs.microsoft.com/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



A new 2D skew transform object has a static value of zero for the AngleX, AngleY, CenterX, and CenterY properties.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh449178(v=vs.85)">IDCompositionVisual::SetTransform</a>
 

 

