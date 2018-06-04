---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUIAnimationVariableCurveChangeHandler2::OnCurveChanged


## -description



         Handles events that occur when the animation curve of an animation variable changes.


## -parameters




### -param variable [in]

The animation variable for which the animation curve has been updated.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -see-also




<a href="https://msdn.microsoft.com/98C95C85-30C9-4E3E-82FE-E3D4C7ECAE0B">IUIAnimationVariable2::SetVariableCurveChangeHandler</a>



<a href="https://msdn.microsoft.com/C3F992CE-6C12-40AF-BA22-10C82E597314">IUIAnimationVariableCurveChangeHandler2</a>
 

 

