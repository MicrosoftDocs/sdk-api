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

# CompositingMode enumeration


## -description


The <b>CompositingMode</b> enumeration specifies how rendered colors are combined with background colors. This enumeration is used by the <a href="https://msdn.microsoft.com/dbc105a5-7541-491c-a8f0-fadecd1670cb">Graphics::GetCompositingMode</a> and <a href="https://msdn.microsoft.com/93367fac-4f61-4082-9f67-13028f1b8a94">Graphics::SetCompositingMode</a> methods of the 
			<b>Graphics</b> class.


## -enum-fields




### -field CompositingModeSourceOver

Specifies that when a color is rendered, it is blended with the background color. The blend is determined by the alpha component of the color being rendered. 


### -field CompositingModeSourceCopy

Specifies that when a color is rendered, it overwrites the background color. This mode cannot be used along with TextRenderingHintClearTypeGridFit. 


## -see-also




<a href="https://msdn.microsoft.com/dbc105a5-7541-491c-a8f0-fadecd1670cb">Graphics::GetCompositingMode</a>



<a href="https://msdn.microsoft.com/93367fac-4f61-4082-9f67-13028f1b8a94">Graphics::SetCompositingMode</a>



<a href="https://msdn.microsoft.com/7f0c88f2-106f-4045-a6eb-cd84cab150c4">TextRenderingHint</a>
 

 

