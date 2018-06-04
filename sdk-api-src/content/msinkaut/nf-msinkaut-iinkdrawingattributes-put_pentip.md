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

# IInkDrawingAttributes::put_PenTip


## -description



Gets or sets a value that indicates which pen tip to use when drawing ink that is associated with this <a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes</a> object.



This property is read/write.


## -parameters


## -remarks



For a complete list of pen tips available to use, see the <a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">InkPenTip</a> enumeration.

When this property is set to <a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">InkPenTip.IPT_Ball</a>, the <a href="https://msdn.microsoft.com/library/windows/hardware/ff542686">Height</a> property is ignored.

To create a square pen tip, set the <b>PenTip</b> property to <a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">InkPenTip.IPT_Rectangle</a>. Then set the <a href="https://msdn.microsoft.com/library/windows/hardware/ff542686">Height</a> property equal to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553316">Width</a> property.




## -see-also




<a href="https://msdn.microsoft.com/2dc9eb94-649f-42f6-8180-abf570bdc757">Height Property [InkDrawingAttributes Class]</a>



<a href="tablet.iinkdrawingattributes">IInkDrawingAttributes</a>



<a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes Class</a>



<a href="https://msdn.microsoft.com/1e68f701-f012-40bb-8ee4-a47da80cb8d6">InkPenTip Enumeration</a>



<a href="https://msdn.microsoft.com/6069f9d3-061a-48ba-8161-86d6152d68f0">Width Property [InkDrawingAttributes Class]</a>
 

 

