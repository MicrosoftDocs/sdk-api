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

# IDirectManipulationContent::GetContentRect


## -description


Retrieves the bounding rectangle of the content, relative to the bounding rectangle of the viewport (if defined).


## -parameters




### -param contentSize [out]

The bounding rectangle of the content.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If the bounding rectangle  has not been set using <a href="https://msdn.microsoft.com/41b14e56-ba24-4ad2-9dac-28daf7d13c6a">SetContentRect</a>, then <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">UI_E_VALUE_NOT_SET</a> is returned. However, the actual content rectangle is (-<a href="_pluslang_Floating_Limits">FLT_MAX</a>, -<a href="_pluslang_Floating_Limits">FLT_MAX</a>, <a href="_pluslang_Floating_Limits">FLT_MAX</a>, <a href="_pluslang_Floating_Limits">FLT_MAX</a>).




## -see-also




<a href="https://msdn.microsoft.com/4d69a503-f998-4197-824f-4df48825c941">IDirectManipulationContent</a>
 

 

