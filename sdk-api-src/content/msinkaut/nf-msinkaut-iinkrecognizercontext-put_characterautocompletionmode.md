---
UID: NF:msinkaut.IInkRecognizerContext.put_CharacterAutoCompletionMode
title: IInkRecognizerContext::put_CharacterAutoCompletionMode (msinkaut.h)
author: windows-sdk-content
description: Gets or sets the character Autocomplete mode, which determines when characters or words are recognized.
old-location: tablet\inkrecognizercontext_characterautocompletion.htm
tech.root: tablet
ms.assetid: 8cb3e41f-803f-4f88-81bb-b2222c070610
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 8cb3e41f-803f-4f88-81bb-b2222c070610, CharacterAutoCompletionMode property [Tablet PC], CharacterAutoCompletionMode property [Tablet PC],IInkRecognizerContext interface, IInkRecognizerContext interface [Tablet PC],CharacterAutoCompletionMode property, IInkRecognizerContext.CharacterAutoCompletionMode, IInkRecognizerContext.put_CharacterAutoCompletionMode, IInkRecognizerContext::CharacterAutoCompletionMode, IInkRecognizerContext::get_CharacterAutoCompletionMode, IInkRecognizerContext::put_CharacterAutoCompletionMode, InkRecognizerContext.get_CharacterAutoCompletion, InkRecognizerContext.put_CharacterAutoCompletion, get_CharacterAutoCompletionMode, msinkaut/IInkRecognizerContext::CharacterAutoCompletionMode, msinkaut/IInkRecognizerContext::get_CharacterAutoCompletionMode, msinkaut/IInkRecognizerContext::put_CharacterAutoCompletionMode, put_CharacterAutoCompletionMode, tablet.inkrecognizercontext_characterautocompletion
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognizerContext::put_CharacterAutoCompletionMode


## -description



Gets or sets the character Autocomplete mode, which determines when characters or words are recognized.



This property is read/write.


## -parameters


## -remarks



Recognition can occur in <a href="https://msdn.microsoft.com/69677379-6700-4128-9e8e-675a9a61a25e">Full</a> mode (all strokes have been inputted), <b>Partial</b> mode (partial input in specific order), or <b>Random</b> mode (partial input in random order).

For a list of the character Autocomplete mode values that you can use, see the <a href="https://msdn.microsoft.com/69677379-6700-4128-9e8e-675a9a61a25e">InkRecognizerCharacterAutoCompletionMode</a> enumeration type.

You cannot turn character Autocomplete off after it is set.

You must set the <a href="https://msdn.microsoft.com/706d28c3-fc5d-496a-a957-daf5ba8d47ca">Guide</a> property before using this property.

Some recognizers do not support character Autocomplete. The <a href="https://msdn.microsoft.com/df405aeb-fefd-4bba-9c02-c1865418f76a">InkRecognizerCapabilities</a> enumeration contains flags for features a recognizer can support. You can determine if the recognizer supports character Autocomplete by checking the value of the <a href="https://msdn.microsoft.com/c8662817-0a33-4828-8de7-c4ce259738a7">Capabilities</a> property.




## -see-also




<a href="https://msdn.microsoft.com/c8662817-0a33-4828-8de7-c4ce259738a7">Capabilities Property</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt846801(v=VS.85).aspx">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/69677379-6700-4128-9e8e-675a9a61a25e">InkRecognizerCharacterAutoCompletionMode Enumeration</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>
 

 

