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

# IInkDisp::put_Dirty


## -description



Gets or sets the value that specifies whether the strokes of an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a> object have been modified since the last time the ink was saved.



This property is read/write.


## -parameters


## -remarks



After ink is saved, the dirty flag is automatically cleared and the value of this property is <b>VARIANT_FALSE</b>. To save ink, call the <a href="https://msdn.microsoft.com/31da19a7-207f-4f11-9b0f-7402e9727f59">Save Method</a> method.




## -see-also




<a href="tablet.iinkdisp">IInkDisp</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/31da19a7-207f-4f11-9b0f-7402e9727f59">Save Method</a>
 

 

