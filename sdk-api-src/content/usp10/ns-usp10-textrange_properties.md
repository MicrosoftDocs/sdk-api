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

# textrange_properties structure


## -description



Contains a group of OpenType features to apply to a run.




## -struct-fields




### -field potfRecords

Pointer to an array of <a href="https://msdn.microsoft.com/3f4d76f7-fd50-4a38-973b-329e477e5960">OPENTYPE_FEATURE_RECORD</a> structures containing OpenType features (records) to apply to the characters in a specific range of text in a run.


### -field cotfRecords

 Number of features in the array specified by <b>potfRecords</b>.


## -see-also




<a href="https://msdn.microsoft.com/3f4d76f7-fd50-4a38-973b-329e477e5960">OPENTYPE_FEATURE_RECORD</a>



<a href="https://msdn.microsoft.com/dd456988-ec9d-4e62-a93f-753ac08a18d9">ScriptPlaceOpenType</a>



<a href="https://msdn.microsoft.com/d2e062a6-2ec8-4057-b525-d1cd719dc736">ScriptShapeOpenType</a>



<a href="https://msdn.microsoft.com/de7a882f-ed74-4be2-b66d-59c2e50dc07a">Uniscribe</a>



<a href="https://msdn.microsoft.com/243438fd-5bb2-4b2a-8b33-803029085adb">Uniscribe Structures</a>
 

 

