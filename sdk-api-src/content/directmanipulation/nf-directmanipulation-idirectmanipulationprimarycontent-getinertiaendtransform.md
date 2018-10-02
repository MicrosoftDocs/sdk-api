---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.GetInertiaEndTransform
title: IDirectManipulationPrimaryContent::GetInertiaEndTransform
author: windows-sdk-content
description: Gets the final transform, including inertia, of the primary content.
old-location: directmanipulation\idirectmanipulationprimarycontent_getinertiaendtransform.htm
tech.root: directmanipulation
ms.assetid: BCF0E48F-C47E-42BE-90F8-25737301DC9C
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetInertiaEndTransform, GetInertiaEndTransform method [Direct Manipulation], GetInertiaEndTransform method [Direct Manipulation],IDirectManipulationPrimaryContent interface, IDirectManipulationPrimaryContent interface [Direct Manipulation],GetInertiaEndTransform method, IDirectManipulationPrimaryContent.GetInertiaEndTransform, IDirectManipulationPrimaryContent::GetInertiaEndTransform, directmanipulation.idirectmanipulationprimarycontent_getinertiaendtransform, directmanipulation/IDirectManipulationPrimaryContent::GetInertiaEndTransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationPrimaryContent.GetInertiaEndTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationPrimaryContent::GetInertiaEndTransform


## -description


Gets the final transform, including inertia, of the primary content.


## -parameters




### -param matrix [out]

The transformed matrix that represents the inertia ending position.


### -param pointCount [in]

The size of the matrix. 

 This value is always 6, because a 3x2 matrix is used for all direct manipulation transforms.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



<div class="alert"><b>Warning</b>  Calling this method can cause a race condition if inertia has ended or been interrupted. This can also occur during the <a href="https://msdn.microsoft.com/7fe7106d-1b13-4a3e-8841-550e0ef55f95">OnViewportStatusChanged</a> callback.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>
 

 

