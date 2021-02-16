---
UID: NF:tom.ITextRange.IsEqual
title: ITextRange::IsEqual (tom.h)
description: Determines whether this range has the same character positions and story as those of a specified range.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","IsEqual method","ITextRange.IsEqual","ITextRange::IsEqual","IsEqual","IsEqual method [Windows Controls]","IsEqual method [Windows Controls]","ITextRange interface","_win32_ITextRange_IsEqual","_win32_ITextRange_IsEqual_cpp","controls.ITextRange_IsEqual","controls._win32_ITextRange_IsEqual","tom/ITextRange::IsEqual"]
old-location: controls\ITextRange_IsEqual.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextrange\itextrangeisequal.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],IsEqual method, ITextRange.IsEqual, ITextRange::IsEqual, IsEqual, IsEqual method [Windows Controls], IsEqual method [Windows Controls],ITextRange interface, _win32_ITextRange_IsEqual, _win32_ITextRange_IsEqual_cpp, controls.ITextRange_IsEqual, controls._win32_ITextRange_IsEqual, tom/ITextRange::IsEqual
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRange::IsEqual
 - tom/ITextRange::IsEqual
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextRange.IsEqual
---

# ITextRange::IsEqual


## -description

Determines whether this range has the same character positions and story as those of a specified range.

## -parameters

### -param pRange

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>*</b>

The <a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a> object that is compared to this range.

### -param pValue

Type: <b>long*</b>

The comparison result. The pointer can be null. The <i>pB</i> parameter receives <b>tomTrue</b> if this range points at the same text (has the same start and end character positions and story) as <i>pRange</i>; otherwise it returns <b>tomFalse</b>.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the ranges have the same character positions and story, the method returns <b>S_OK</b>. Otherwise, it returns S_FALSE.

## -remarks

The 
				<b>ITextRange::IsEqual</b> method returns <b>tomTrue</b> only if the range points at the same text as <i>pRange</i>. See <a href="/windows/desktop/Controls/about-text-object-model">Finding Rich Text</a> for code that compares two different pieces of text to see if they contain the same plain text and the same character formatting.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>