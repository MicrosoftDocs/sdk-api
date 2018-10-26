---
UID: NE:msinkaut.InkRecognizerCharacterAutoCompletionMode
title: InkRecognizerCharacterAutoCompletionMode
author: windows-sdk-content
description: Specifies types of character input modes.
old-location: tablet\inkrecognizercharacterautocompletionmode.htm
tech.root: tablet
ms.assetid: 69677379-6700-4128-9e8e-675a9a61a25e
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: 69677379-6700-4128-9e8e-675a9a61a25e, IRCACM_Full, IRCACM_Prefix, IRCACM_Random, InkRecognizerCharacterAutoCompletionMode, InkRecognizerCharacterAutoCompletionMode enumeration [Tablet PC], msinkaut/IRCACM_Full, msinkaut/IRCACM_Prefix, msinkaut/IRCACM_Random, msinkaut/InkRecognizerCharacterAutoCompletionMode, tablet.inkrecognizercharacterautocompletionmode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkRecognizerCharacterAutoCompletionMode
product: Windows
targetos: Windows
req.typenames: InkRecognizerCharacterAutoCompletionMode
req.redist: 
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
 

 

