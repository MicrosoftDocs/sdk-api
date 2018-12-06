---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetSnapPoints
title: IDirectManipulationPrimaryContent::SetSnapPoints
author: windows-sdk-content
description: Specifies the snap points for the inertia rest position.
old-location: directmanipulation\idirectmanipulationprimarycontent_setsnappoints.htm
tech.root: directmanipulation
ms.assetid: 3257952d-903b-455c-9422-9739411a5924
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetSnapPoints method, IDirectManipulationPrimaryContent.SetSnapPoints, IDirectManipulationPrimaryContent::SetSnapPoints, SetSnapPoints, SetSnapPoints method [Direct Manipulation], SetSnapPoints method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_setsnappoints, directmanipulation/IDirectManipulationPrimaryContent::SetSnapPoints
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
 - IDirectManipulationPrimaryContent.SetSnapPoints
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationPrimaryContent::SetSnapPoints


## -description


Specifies the snap points for the inertia rest position.


## -parameters




### -param motion [in]

One or more of the <a href="https://msdn.microsoft.com/a0b4da55-3ebb-4281-a372-4bc6b91e6789">DIRECTMANIPULATION_MOTION_TYPES</a> enumeration values. Only <b>DIRECTMANIPULATION_MOTION_TRANSLATE_X</b>, <b>DIRECTMANIPULATION_MOTION_TRANSLATE_Y</b>, or <b>DIRECTMANIPULATION_MOTION_ZOOM</b> are allowed.


### -param points [in]

An array of snap points within the boundaries of the content to snap to. Should be specified in increasing order relative to the origin set in <a href="https://msdn.microsoft.com/3f9afe1b-20f4-45fa-a63b-25b7a0c597af">SetSnapCoordinate</a>.


### -param pointCount [in]

 The size of the array of snap points. Should be greater than 0.


## -returns



If the method succeeds, it returns <b>S_OK</b>. If there is no change in the snap points, this method can return <b>S_FALSE</b>. Otherwise, it returns an <b>HRESULT</b> error code. If invalid snap points are specified, existing snap points might be affected.




## -remarks



If snap points are invalid (for example, outside of the content boundaries), they are ignored and the content is always within the content boundaries. 




## -see-also




<a href="https://msdn.microsoft.com/9910F5F5-950F-4099-9808-B46FA5BBA6FB">IDirectManipulationPrimaryContent</a>



<a href="https://msdn.microsoft.com/3f9afe1b-20f4-45fa-a63b-25b7a0c597af">SetSnapCoordinate</a>



<a href="https://msdn.microsoft.com/99d039fe-017a-47c5-95a1-5000efe92ba0">SetSnapInterval</a>
 

 

