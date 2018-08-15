---
UID: NF:directmanipulation.IDirectManipulationContent.SyncContentTransform
title: IDirectManipulationContent::SyncContentTransform
author: windows-sdk-content
description: Modifies the content transform while maintaining the output transform.
old-location: directmanipulation\idirectmanipulationcontent_synccontenttransform.htm
old-project: directmanipulation
ms.assetid: 3e70b208-05b5-4b84-a582-fd835acdd777
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDirectManipulationContent interface [Direct Manipulation],SyncContentTransform method, IDirectManipulationContent.SyncContentTransform, IDirectManipulationContent::SyncContentTransform, SyncContentTransform, SyncContentTransform method [Direct Manipulation], SyncContentTransform method [Direct Manipulation],IDirectManipulationContent interface, directmanipulation.idirectmanipulationcontent_synccontenttransform, directmanipulation/IDirectManipulationContent::SyncContentTransform
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DIRECTMANIPULATION_VIEWPORT_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationContent.SyncContentTransform
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDirectManipulationContent::SyncContentTransform


## -description


Modifies the content transform while maintaining the output transform.


## -parameters




### -param matrix [in]

The transform matrix.


### -param pointCount [in]

The size of the transform matrix. This value is always 6, because a 3x2 matrix is used for all direct manipulation transforms.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method will fail if the viewport state is <a href="https://msdn.microsoft.com/6120702f-56f0-489d-a3b2-5f6ecac82b5e">DIRECTMANIPULATION_RUNNING</a>, <b>DIRECTMANIPULATION_INERTIA</b> or <b>DIRECTMANIPULATION_SUSPENDED</b>.

This method is useful when the application wants to apply transforms on top of the content transforms at the end of a manipulation, while preserving the visual output transform of the content.






## -see-also




<a href="https://msdn.microsoft.com/4d69a503-f998-4197-824f-4df48825c941">IDirectManipulationContent</a>
 

 

