---
UID: NE:msinkaut.InkRecognizerCharacterAutoCompletionMode
title: InkRecognizerCharacterAutoCompletionMode (msinkaut.h)
description: Specifies types of character input modes.
helpviewer_keywords: ["69677379-6700-4128-9e8e-675a9a61a25e","IRCACM_Full","IRCACM_Prefix","IRCACM_Random","InkRecognizerCharacterAutoCompletionMode","InkRecognizerCharacterAutoCompletionMode enumeration [Tablet PC]","msinkaut/IRCACM_Full","msinkaut/IRCACM_Prefix","msinkaut/IRCACM_Random","msinkaut/InkRecognizerCharacterAutoCompletionMode","tablet.inkrecognizercharacterautocompletionmode"]
old-location: tablet\inkrecognizercharacterautocompletionmode.htm
tech.root: tablet
ms.assetid: 69677379-6700-4128-9e8e-675a9a61a25e
ms.date: 12/05/2018
ms.keywords: 69677379-6700-4128-9e8e-675a9a61a25e, IRCACM_Full, IRCACM_Prefix, IRCACM_Random, InkRecognizerCharacterAutoCompletionMode, InkRecognizerCharacterAutoCompletionMode enumeration [Tablet PC], msinkaut/IRCACM_Full, msinkaut/IRCACM_Prefix, msinkaut/IRCACM_Random, msinkaut/InkRecognizerCharacterAutoCompletionMode, tablet.inkrecognizercharacterautocompletionmode
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
targetos: Windows
req.typenames: InkRecognizerCharacterAutoCompletionMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkRecognizerCharacterAutoCompletionMode
 - msinkaut/InkRecognizerCharacterAutoCompletionMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msinkaut.h
api_name:
 - InkRecognizerCharacterAutoCompletionMode
---

# InkRecognizerCharacterAutoCompletionMode enumeration


## -description

Specifies types of character input modes.

## -enum-fields

### -field IRCACM_Full:0

Recognition occurs as if all strokes have been input.

### -field IRCACM_Prefix

Recognition occurs on partial input. The order of the strokes must conform to the rules of the language.

### -field IRCACM_Random

Recognition occurs on partial input. The order of the strokes can be arbitrary.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_characterautocompletionmode">CharacterAutoCompletion Property [InkRecognizerContext Class]</a>



<a href="/windows/desktop/tablet/inkrecognizercontext-class">InkRecognizerContext Class</a>
