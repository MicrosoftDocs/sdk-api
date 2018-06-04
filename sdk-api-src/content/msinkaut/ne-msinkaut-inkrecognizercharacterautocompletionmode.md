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

# InkRecognizerCharacterAutoCompletionMode enumeration


## -description



Specifies types of character input modes.




## -enum-fields




### -field IRCACM_Full

Recognition occurs as if all strokes have been input.


### -field IRCACM_Prefix

Recognition occurs on partial input. The order of the strokes must conform to the rules of the language.


### -field IRCACM_Random

Recognition occurs on partial input. The order of the strokes can be arbitrary.


## -see-also




<a href="https://msdn.microsoft.com/8cb3e41f-803f-4f88-81bb-b2222c070610">CharacterAutoCompletion Property [InkRecognizerContext Class]</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

