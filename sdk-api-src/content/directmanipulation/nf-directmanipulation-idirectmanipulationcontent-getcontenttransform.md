---
UID: NF:directmanipulation.IDirectManipulationContent.GetContentTransform
title: IDirectManipulationContent::GetContentTransform
author: windows-sdk-content
description: Retrieves the transform applied to the content.
old-location: directmanipulation\idirectmanipulationcontent_getcontenttransform.htm
tech.root: directmanipulation
ms.assetid: 9db4f521-227c-4e2f-8c7d-44ae4a25651e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetContentTransform, GetContentTransform method [Direct Manipulation], GetContentTransform method [Direct Manipulation],IDirectManipulationContent interface, IDirectManipulationContent interface [Direct Manipulation],GetContentTransform method, IDirectManipulationContent.GetContentTransform, IDirectManipulationContent::GetContentTransform, directmanipulation.idirectmanipulationcontent_getcontenttransform, directmanipulation/IDirectManipulationContent::GetContentTransform
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
 - IDirectManipulationContent.GetContentTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationContent::GetContentTransform


## -description


    Retrieves the transform applied to the content.


## -parameters




### -param matrix [out]

The transform matrix.


### -param pointCount [in]

The size of the transform matrix. This value is always 6, because a 3x2 matrix is used for all direct manipulation transforms.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This transform contains the default overpan and bounce curves during manipulation and inertia.

This transform does not contain the sync transform set with <a href="https://msdn.microsoft.com/3e70b208-05b5-4b84-a582-fd835acdd777">SyncContentTransform</a>.



When this method returns, the format of <i>matrix</i> is:

<i>matrix</i>
<i>matrix</i>
<i>matrix</i>
<i>matrix</i>
<i>matrix</i>
<i>matrix</i>



## -see-also




<a href="https://msdn.microsoft.com/4d69a503-f998-4197-824f-4df48825c941">IDirectManipulationContent</a>
 

 

