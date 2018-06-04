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

# _MFVideoSrcContentHintFlags enumeration


## -description



Describes the intended aspect ratio for a video stream.




## -enum-fields




### -field MFVideoSrcContentHintFlag_None

The aspect ratio is unknown.


### -field MFVideoSrcContentHintFlag_16x9

The source is 16×9 content encoded within a 4×3 area.


### -field MFVideoSrcContentHintFlag_235_1

The source is 2.35:1 content encoded within a 16×9 or 4×3 area.


## -remarks



Use these flags with the <a href="https://msdn.microsoft.com/6b32e257-c523-4859-8c8f-661c33810624">MF_MT_SOURCE_CONTENT_HINT</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

