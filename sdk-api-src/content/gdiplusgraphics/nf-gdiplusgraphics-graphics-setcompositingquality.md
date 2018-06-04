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

# Graphics::SetCompositingQuality


## -description


The <b>Graphics::SetCompositingQuality</b> method sets the compositing quality of this <a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> object.


## -parameters




### -param compositingQuality [in]

Type: <b><a href="https://msdn.microsoft.com/d5e0e6ff-9b82-45e2-bcf6-3d66a509eba7">CompositingQuality</a></b>

Element of the <a href="https://msdn.microsoft.com/d5e0e6ff-9b82-45e2-bcf6-3d66a509eba7">CompositingQuality</a> enumeration that specifies the compositing quality. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration. 




## -see-also




<a href="https://msdn.microsoft.com/f8c22d1a-b96b-4d16-928e-20adbae4c4a7">Alpha Blending Lines and Fills</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a>



<a href="https://msdn.microsoft.com/dbc105a5-7541-491c-a8f0-fadecd1670cb">Graphics::GetCompositingMode</a>



<a href="https://msdn.microsoft.com/7d37da31-6ab0-4054-8a98-64cfbf9225ec">Graphics::GetCompositingQuality</a>



<a href="https://msdn.microsoft.com/93367fac-4f61-4082-9f67-13028f1b8a94">Graphics::SetCompositingMode</a>



<a href="https://msdn.microsoft.com/6e633cb2-8b0f-4b6a-95d8-f494d5f972eb">HatchBrush</a>



<a href="https://msdn.microsoft.com/0257a23c-560e-472e-863a-6ab5881dc156">New Features</a>



<a href="https://msdn.microsoft.com/8d5c8780-f03c-40b2-b237-e40121e3d6f6">SolidBrush</a>
 

 

