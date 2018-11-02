---
UID: NF:dcomp.IDCompositionDevice2.CreateTranslateTransform3D
title: IDCompositionDevice2::CreateTranslateTransform3D
author: windows-sdk-content
description: Creates a 3D translation transform object.
old-location: directcomp\idcompositiondevice2_createtranslatetransform3d.htm
tech.root: directcomp
ms.assetid: 7913D11B-5563-4921-B455-C34069AC7BCD
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CreateTranslateTransform3D, CreateTranslateTransform3D method [DirectComposition], CreateTranslateTransform3D method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateTranslateTransform3D method, IDCompositionDevice2.CreateTranslateTransform3D, IDCompositionDevice2::CreateTranslateTransform3D, dcomp/IDCompositionDevice2::CreateTranslateTransform3D, directcomp.idcompositiondevice2_createtranslatetransform3d
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IDCompositionDevice2.CreateTranslateTransform3D
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDCompositionDevice2::CreateTranslateTransform3D


## -description


Creates a 3D translation transform object.


## -parameters




### -param translateTransform3D [out]

Type: <b><a href="https://msdn.microsoft.com/C265E5FC-F7A1-4E87-8311-C4D0613DD7BC">IDCompositionTranslateTransform3D</a>**</b>

The new 3D translation transform object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A newly created 3D translation transform has a static value of 0 for the OffsetX, OffsetY, and OffsetZ properties.








## -see-also




<a href="https://msdn.microsoft.com/0E5D0AEC-63A3-4A44-9A0B-D1E26789CAB0">IDCompositionDevice2</a>



<a href="https://msdn.microsoft.com/40935581-D45C-496B-90B9-152963F0B55A">IDCompositionEffectGroup::SetTransform3D</a>



<a href="https://msdn.microsoft.com/CCA785F6-869C-460A-AF54-573BDE798685">IDCompositionVisual::SetEffect</a>
 

 

