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

# IInkEdit::put_SelInks


## -description



Gets or sets the array of embedded <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> objects (if displayed as ink) in the current selection.



This property is read/write.


## -parameters


## -remarks



Ink must be recognized before being accessed through this property. If it is not recognized first, the <b>SelInks</b> property always contains zero <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> objects. You must either call the <a href="https://msdn.microsoft.com/e22043da-6c38-49e2-9651-43211ce7f377">Recognize</a> method (if the <a href="https://msdn.microsoft.com/e1171aa3-841f-433e-88b8-e3fc63129aeb">RecognitionTimeout</a> property equals 0) or wait until the ink is automatically recognized (when the value of the <b>RecognitionTimeout</b> property is greater than 0) to access ink through this property.

The <a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a> control ignores any <a href="https://msdn.microsoft.com/10ca7ae5-28dd-42a2-98d9-852d4de5869d">InkDrawingAttributes</a> on ink set through the <b>SelInks</b> property. Instead, the InkEdit control applies alternate drawing attributes according to the attributes of nearby text.

This property is run time only.




## -see-also




<a href="tablet.iinkedit_">IInkEdit</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/52761cb2-4433-4824-ba19-fe597de2faf0">InkEdit</a>



<a href="https://msdn.microsoft.com/e1171aa3-841f-433e-88b8-e3fc63129aeb">RecoTimeout Property</a>



<a href="https://msdn.microsoft.com/e22043da-6c38-49e2-9651-43211ce7f377">Recognize Method [InkEdit Control]</a>
 

 

