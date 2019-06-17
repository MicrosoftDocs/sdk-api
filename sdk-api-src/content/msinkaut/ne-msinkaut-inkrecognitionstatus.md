---
UID: NE:msinkaut.InkRecognitionStatus
title: InkRecognitionStatus (msinkaut.h)
author: windows-sdk-content
description: Specifies whether an error occurred during recognition and, if so, which error occurred.
old-location: tablet\inkrecognitionstatus.htm
tech.root: tablet
ms.assetid: d6ff29a8-d100-4bfe-848b-941367d8b2dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRS_InkAddedFailed, IRS_Interrupted, IRS_NoError, IRS_ProcessFailed, IRS_SetAutoCompletionModeFailed, IRS_SetFactoidFailed, IRS_SetFlagsFailed, IRS_SetGuideFailed, IRS_SetPrefixSuffixFailed, IRS_SetStrokesFailed, IRS_SetWordListFailed, InkRecognitionStatus, InkRecognitionStatus enumeration [Tablet PC], d6ff29a8-d100-4bfe-848b-941367d8b2dd, msinkaut/IRS_InkAddedFailed, msinkaut/IRS_Interrupted, msinkaut/IRS_NoError, msinkaut/IRS_ProcessFailed, msinkaut/IRS_SetAutoCompletionModeFailed, msinkaut/IRS_SetFactoidFailed, msinkaut/IRS_SetFlagsFailed, msinkaut/IRS_SetGuideFailed, msinkaut/IRS_SetPrefixSuffixFailed, msinkaut/IRS_SetStrokesFailed, msinkaut/IRS_SetWordListFailed, msinkaut/InkRecognitionStatus, tablet.inkrecognitionstatus
ms.topic: enum
f1_keywords: ["msinkaut/InkRecognitionStatus"]
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
 - InkRecognitionStatus
product: Windows
targetos: Windows
req.typenames: InkRecognitionStatus
req.redist: 
ms.custom: 19H1
---

# InkRecognitionStatus enumeration


## -description



Specifies whether an error occurred during recognition and, if so, which error occurred.




## -enum-fields




### -field IRS_NoError

Specifies no error.


### -field IRS_Interrupted

The recognition was interrupted by a call to <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-stopbackgroundrecognition">StopBackgroundRecognition</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode">CharacterAutoCompletion Property [InkRecognizerContext Class]</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid">Factoid Property [InkRecognizerContext Class]</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide">Guide Property [InkRecognizerContext Class]</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext">PrefixText Property [InkRecognizerContext Class]</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkrecognizercontext-recognition">Recognition Event [InkRecognizerContext Class]</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags">RecognitionFlags Property [InkRecognizerContext Class]</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext">SuffixText Property [InkRecognizerContext Class]</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist">WordList Property [InkRecognizerContext Class]</a>
 

 

