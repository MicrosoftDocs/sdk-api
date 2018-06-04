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

# InkRecognitionStatus enumeration


## -description



Specifies whether an error occurred during recognition and, if so, which error occurred.




## -enum-fields




### -field IRS_NoError

Specifies no error.


### -field IRS_Interrupted

The recognition was interrupted by a call to <a href="https://msdn.microsoft.com/25ece9a1-cbc3-43ae-85ec-e3bf78a4e5a0">StopBackgroundRecognition</a>.


### -field IRS_ProcessFailed

The ink recognition process failed.


### -field IRS_InkAddedFailed

The ink could not be added.


### -field IRS_SetAutoCompletionModeFailed

The <i>character Autocomplete</i> mode could not be set.


### -field IRS_SetStrokesFailed

The strokes could not be set.


### -field IRS_SetGuideFailed

The recognition guide could not be set.


### -field IRS_SetFlagsFailed

The flags could not be set.


### -field IRS_SetFactoidFailed

The factoid could not be set.


### -field IRS_SetPrefixSuffixFailed

The suffix or the prefix could not be set.


### -field IRS_SetWordListFailed

The word list could not be set.


## -remarks



The SetGuideFailed, SetFlagsFailed, SetFactoidFailed, and SetPrefixSuffixFailed members are redundant because an error is also raised when the corresponding properties are set.




## -see-also




<a href="https://msdn.microsoft.com/8cb3e41f-803f-4f88-81bb-b2222c070610">CharacterAutoCompletion Property [InkRecognizerContext Class]</a>



<a href="https://msdn.microsoft.com/11a76706-e2e5-4ae5-bdc2-5354514ea29f">Factoid Property [InkRecognizerContext Class]</a>



<a href="https://msdn.microsoft.com/706d28c3-fc5d-496a-a957-daf5ba8d47ca">Guide Property [InkRecognizerContext Class]</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/fe5c91ce-c53e-4f33-bd67-2f1c10e5cf97">PrefixText Property [InkRecognizerContext Class]</a>



<a href="https://msdn.microsoft.com/0cc319af-cd0b-4089-928b-cae6c86f6f61">Recognition Event [InkRecognizerContext Class]</a>



<a href="https://msdn.microsoft.com/71b02f99-4076-4c56-b88a-4201b7033411">RecognitionFlags Property [InkRecognizerContext Class]</a>



<a href="https://msdn.microsoft.com/f7fb1314-b5d5-4aa9-91d0-cbd649aded39">SuffixText Property [InkRecognizerContext Class]</a>



<a href="https://msdn.microsoft.com/893950d4-c19c-4635-ad66-6e363860280a">WordList Property [InkRecognizerContext Class]</a>
 

 

