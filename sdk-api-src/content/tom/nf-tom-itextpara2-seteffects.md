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

# ITextPara2::SetEffects


## -description


Sets the paragraph format effects.


## -parameters




### -param Value [in]

Type: <b>long</b>

The paragraph effects value.

This value can be a combination of the flags defined in the table for <a href="https://msdn.microsoft.com/7f672cc9-e8f3-416a-8f41-9b71ca1858a1">ITextPara2::GetEffects</a>.


### -param Mask [in]

Type: <b>long</b>

The desired mask.

This value can be a combination of the flags defined in the table for <a href="https://msdn.microsoft.com/7f672cc9-e8f3-416a-8f41-9b71ca1858a1">ITextPara2::GetEffects</a>. 

Only effects with the corresponding mask flag set are modified.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/31a0849f-c651-4178-b1ff-a4333bcde5d9">ITextPara2</a>



<a href="https://msdn.microsoft.com/7f672cc9-e8f3-416a-8f41-9b71ca1858a1">ITextPara2::GetEffects</a>
 

 

