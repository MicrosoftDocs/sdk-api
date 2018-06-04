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

# InkExtractFlags enumeration


## -description



Determines how a stroke is removed from an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.




## -enum-fields




### -field IEF_CopyFromOriginal

The ink is copied from the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.


### -field IEF_RemoveFromOriginal

The ink is cut from the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.


### -field IEF_Default

The ink is cut from the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object.


## -remarks



This enumeration is a flag.




## -see-also




<a href="https://msdn.microsoft.com/1cb109e5-5193-4022-a3b1-ade9be1337e8">ExtractStrokes Method</a>



<a href="https://msdn.microsoft.com/b32467a8-a677-4a80-8029-d364e6e372c6">ExtractWithRectangle Method</a>
 

 

