---
UID: NE:msinkaut.InkRecognitionStatus
title: InkRecognitionStatus
author: windows-sdk-content
description: Specifies whether an error occurred during recognition and, if so, which error occurred.
old-location: tablet\inkrecognitionstatus.htm
old-project: tablet
ms.assetid: d6ff29a8-d100-4bfe-848b-941367d8b2dd
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: IRS_InkAddedFailed, IRS_Interrupted, IRS_NoError, IRS_ProcessFailed, IRS_SetAutoCompletionModeFailed, IRS_SetFactoidFailed, IRS_SetFlagsFailed, IRS_SetGuideFailed, IRS_SetPrefixSuffixFailed, IRS_SetStrokesFailed, IRS_SetWordListFailed, InkRecognitionStatus, InkRecognitionStatus enumeration [Tablet PC], d6ff29a8-d100-4bfe-848b-941367d8b2dd, msinkaut/IRS_InkAddedFailed, msinkaut/IRS_Interrupted, msinkaut/IRS_NoError, msinkaut/IRS_ProcessFailed, msinkaut/IRS_SetAutoCompletionModeFailed, msinkaut/IRS_SetFactoidFailed, msinkaut/IRS_SetFlagsFailed, msinkaut/IRS_SetGuideFailed, msinkaut/IRS_SetPrefixSuffixFailed, msinkaut/IRS_SetStrokesFailed, msinkaut/IRS_SetWordListFailed, msinkaut/InkRecognitionStatus, tablet.inkrecognitionstatus
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
tech.root: 
req.typenames: InkRecognitionStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkRecognitionStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

