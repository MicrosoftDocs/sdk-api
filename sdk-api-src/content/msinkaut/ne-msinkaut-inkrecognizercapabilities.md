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

# InkRecognizerCapabilities enumeration


## -description



Specifies the attributes of a recognizer. You also use this enumeration to determine which attributes to use when you search for an installed recognizer.




## -enum-fields




### -field IRC_DontCare


### -field IRC_Object

The recognizer performs object recognition; otherwise, the recognizer performs text recognition.


### -field IRC_FreeInput

The recognizer supports free input. Ink is entered without the use of a recognition guide, such as lines or boxes.


### -field IRC_LinedInput

The recognizer supports lined input, which is similar to writing on lined paper.


### -field IRC_BoxedInput

The recognizer supports boxed input, in which each character or word is entered in a box.


### -field IRC_CharacterAutoCompletionInput

The recognizer supports character Autocomplete. Recognizers that support character Autocomplete require boxed input.


### -field IRC_RightAndDown

The recognizer supports western and Asian languages.


### -field IRC_LeftAndDown

The recognizer supports Hebrew and Arabic languages.


### -field IRC_DownAndLeft

The recognizer supports Asian languages.


### -field IRC_DownAndRight

The recognizer supports the Chinese language.


### -field IRC_ArbitraryAngle

The recognizer supports text that is written at arbitrary angles.


### -field IRC_Lattice

The recognizer can return a lattice object.


### -field IRC_AdviseInkChange

The recognizer's background recognition can be interrupted, as in when the ink has changed.


### -field IRC_StrokeReorder

Specifies that stroke order - spatial and temporal - is handled.


### -field IRC_Personalizable

The recognizer supports personalization.


### -field IRC_PrefersArbitraryAngle


### -field IRC_PrefersParagraphBreaking


### -field IRC_PrefersSegmentation


### -field IRC_Cursive


### -field IRC_TextPrediction


### -field IRC_Alpha


### -field IRC_Beta




#### - [Hidden] IRC_DontCare

Ignores all other flags that are set.


## -remarks



This enumeration is a flag.




## -see-also




<a href="https://msdn.microsoft.com/c8662817-0a33-4828-8de7-c4ce259738a7">Capabilities Property [IInkRecognizer Interface]</a>



<a href="https://msdn.microsoft.com/706d28c3-fc5d-496a-a957-daf5ba8d47ca">Guide Property [InkRecognizerContext Class]</a>



<a href="https://msdn.microsoft.com/97f982b6-f330-4053-91a9-2a4edc13b4b0">IInkRecognizer Interface</a>
 

 

