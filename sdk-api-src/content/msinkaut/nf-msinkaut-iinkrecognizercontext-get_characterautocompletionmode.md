---
UID: NF:msinkaut.IInkRecognizerContext.get_CharacterAutoCompletionMode
title: IInkRecognizerContext::get_CharacterAutoCompletionMode (msinkaut.h)
description: Gets or sets the character Autocomplete mode, which determines when characters or words are recognized. (Get)
helpviewer_keywords: ["8cb3e41f-803f-4f88-81bb-b2222c070610","CharacterAutoCompletionMode property [Tablet PC]","CharacterAutoCompletionMode property [Tablet PC]","IInkRecognizerContext interface","IInkRecognizerContext interface [Tablet PC]","CharacterAutoCompletionMode property","IInkRecognizerContext.CharacterAutoCompletionMode","IInkRecognizerContext.get_CharacterAutoCompletionMode","IInkRecognizerContext::CharacterAutoCompletionMode","IInkRecognizerContext::get_CharacterAutoCompletionMode","IInkRecognizerContext::put_CharacterAutoCompletionMode","InkRecognizerContext.get_CharacterAutoCompletion","InkRecognizerContext.put_CharacterAutoCompletion","get_CharacterAutoCompletionMode","msinkaut/IInkRecognizerContext::CharacterAutoCompletionMode","msinkaut/IInkRecognizerContext::get_CharacterAutoCompletionMode","msinkaut/IInkRecognizerContext::put_CharacterAutoCompletionMode","put_CharacterAutoCompletionMode","tablet.inkrecognizercontext_characterautocompletion"]
old-location: tablet\inkrecognizercontext_characterautocompletion.htm
tech.root: tablet
ms.assetid: 8cb3e41f-803f-4f88-81bb-b2222c070610
ms.date: 12/05/2018
ms.keywords: 8cb3e41f-803f-4f88-81bb-b2222c070610, CharacterAutoCompletionMode property [Tablet PC], CharacterAutoCompletionMode property [Tablet PC],IInkRecognizerContext interface, IInkRecognizerContext interface [Tablet PC],CharacterAutoCompletionMode property, IInkRecognizerContext.CharacterAutoCompletionMode, IInkRecognizerContext.get_CharacterAutoCompletionMode, IInkRecognizerContext::CharacterAutoCompletionMode, IInkRecognizerContext::get_CharacterAutoCompletionMode, IInkRecognizerContext::put_CharacterAutoCompletionMode, InkRecognizerContext.get_CharacterAutoCompletion, InkRecognizerContext.put_CharacterAutoCompletion, get_CharacterAutoCompletionMode, msinkaut/IInkRecognizerContext::CharacterAutoCompletionMode, msinkaut/IInkRecognizerContext::get_CharacterAutoCompletionMode, msinkaut/IInkRecognizerContext::put_CharacterAutoCompletionMode, put_CharacterAutoCompletionMode, tablet.inkrecognizercontext_characterautocompletion
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRecognizerContext::get_CharacterAutoCompletionMode
 - msinkaut/IInkRecognizerContext::get_CharacterAutoCompletionMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizerContext.CharacterAutoCompletionMode
 - IInkRecognizerContext.get_CharacterAutoCompletionMode
 - IInkRecognizerContext.put_CharacterAutoCompletionMode
 - InkRecognizerContext.get_CharacterAutoCompletion
 - InkRecognizerContext.put_CharacterAutoCompletion
---

# IInkRecognizerContext::get_CharacterAutoCompletionMode


## -description

Gets or sets the character Autocomplete mode, which determines when characters or words are recognized.



This property is read/write.

## -parameters

## -remarks

Recognition can occur in <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode">Full</a> mode (all strokes have been input), <b>Partial</b> mode (partial input in specific order), or <b>Random</b> mode (partial input in random order).

For a list of the character Autocomplete mode values that you can use, see the <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode">InkRecognizerCharacterAutoCompletionMode</a> enumeration type.

You cannot turn character Autocomplete off after it is set.

You must set the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide">Guide</a> property before using this property.

Some recognizers do not support character Autocomplete. The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercapabilities">InkRecognizerCapabilities</a> enumeration contains flags for features a recognizer can support. You can determine if the recognizer supports character Autocomplete by checking the value of the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities">Capabilities</a> property.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities">Capabilities Property</a>



<a href="../msinkaut/nn-msinkaut-iinkrecognizercontext.md">IInkRecognizerContext</a>



<a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode">InkRecognizerCharacterAutoCompletionMode Enumeration</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>
