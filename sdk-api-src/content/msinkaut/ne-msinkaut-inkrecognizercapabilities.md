---
UID: NE:msinkaut.InkRecognizerCapabilities
title: InkRecognizerCapabilities (msinkaut.h)
description: Specifies the attributes of a recognizer. You also use this enumeration to determine which attributes to use when you search for an installed recognizer.
helpviewer_keywords: ["IRC_AdviseInkChange","IRC_ArbitraryAngle","IRC_BoxedInput","IRC_CharacterAutoCompletionInput","IRC_DownAndLeft","IRC_DownAndRight","IRC_FreeInput","IRC_Lattice","IRC_LeftAndDown","IRC_LinedInput","IRC_Object","IRC_Personalizable","IRC_RightAndDown","IRC_StrokeReorder","InkRecognizerCapabilities","InkRecognizerCapabilities enumeration [Tablet PC]","[Hidden] IRC_DontCare","df405aeb-fefd-4bba-9c02-c1865418f76a","msinkaut/IRC_AdviseInkChange","msinkaut/IRC_ArbitraryAngle","msinkaut/IRC_BoxedInput","msinkaut/IRC_CharacterAutoCompletionInput","msinkaut/IRC_DownAndLeft","msinkaut/IRC_DownAndRight","msinkaut/IRC_FreeInput","msinkaut/IRC_Lattice","msinkaut/IRC_LeftAndDown","msinkaut/IRC_LinedInput","msinkaut/IRC_Object","msinkaut/IRC_Personalizable","msinkaut/IRC_RightAndDown","msinkaut/IRC_StrokeReorder","msinkaut/InkRecognizerCapabilities","msinkaut/[Hidden] IRC_DontCare","tablet.inkrecognizercapabilities"]
old-location: tablet\inkrecognizercapabilities.htm
tech.root: tablet
ms.assetid: df405aeb-fefd-4bba-9c02-c1865418f76a
ms.date: 12/05/2018
ms.keywords: IRC_AdviseInkChange, IRC_ArbitraryAngle, IRC_BoxedInput, IRC_CharacterAutoCompletionInput, IRC_DownAndLeft, IRC_DownAndRight, IRC_FreeInput, IRC_Lattice, IRC_LeftAndDown, IRC_LinedInput, IRC_Object, IRC_Personalizable, IRC_RightAndDown, IRC_StrokeReorder, InkRecognizerCapabilities, InkRecognizerCapabilities enumeration [Tablet PC], [Hidden] IRC_DontCare, df405aeb-fefd-4bba-9c02-c1865418f76a, msinkaut/IRC_AdviseInkChange, msinkaut/IRC_ArbitraryAngle, msinkaut/IRC_BoxedInput, msinkaut/IRC_CharacterAutoCompletionInput, msinkaut/IRC_DownAndLeft, msinkaut/IRC_DownAndRight, msinkaut/IRC_FreeInput, msinkaut/IRC_Lattice, msinkaut/IRC_LeftAndDown, msinkaut/IRC_LinedInput, msinkaut/IRC_Object, msinkaut/IRC_Personalizable, msinkaut/IRC_RightAndDown, msinkaut/IRC_StrokeReorder, msinkaut/InkRecognizerCapabilities, msinkaut/[Hidden] IRC_DontCare, tablet.inkrecognizercapabilities
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
req.typenames: InkRecognizerCapabilities
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InkRecognizerCapabilities
 - msinkaut/InkRecognizerCapabilities
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
 - InkRecognizerCapabilities
---

# InkRecognizerCapabilities enumeration


## -description

Specifies the attributes of a recognizer. You also use this enumeration to determine which attributes to use when you search for an installed recognizer.

## -enum-fields

### -field IRC_DontCare

Ignores all other flags that are set.

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




## -remarks

This enumeration is a flag.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities">Capabilities Property [IInkRecognizer Interface]</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_guide">Guide Property [InkRecognizerContext Class]</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer">IInkRecognizer Interface</a>