---
UID: NF:tom.ITextRange.SetStart
title: ITextRange::SetStart (tom.h)
description: Sets the character position for the start of this range.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","SetStart method","ITextRange.SetStart","ITextRange::SetStart","SetStart","SetStart method [Windows Controls]","SetStart method [Windows Controls]","ITextRange interface","_win32_ITextRange_SetStart","_win32_ITextRange_SetStart_cpp","controls.ITextRange_SetStart","controls._win32_ITextRange_SetStart","tom/ITextRange::SetStart"]
old-location: controls\ITextRange_SetStart.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setstart.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],SetStart method, ITextRange.SetStart, ITextRange::SetStart, SetStart, SetStart method [Windows Controls], SetStart method [Windows Controls],ITextRange interface, _win32_ITextRange_SetStart, _win32_ITextRange_SetStart_cpp, controls.ITextRange_SetStart, controls._win32_ITextRange_SetStart, tom/ITextRange::SetStart
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
 - ITextRange::SetStart
 - tom/ITextRange::SetStart
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
 - ITextRange.SetStart
---

# ITextRange::SetStart


## -description

Sets the character  position for the start of this range.

## -parameters

### -param cpFirst [in]

Type: <b>long</b>

The new character position for the start of the range.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE.

## -remarks

Note that if <i>cpFirst</i> is greater than the range's end position, this method sets the end position equal to <i>cpFirst</i>, making the range an insertion point. If this range is the selection, the start position becomes the active end and is scrolled into view if the display isn't frozen.


<a href="/windows/desktop/api/tom/nf-tom-itextrange-setend">ITextRange::SetEnd</a> sets the range's end position, and <a href="/windows/desktop/api/tom/nf-tom-itextrange-setrange">ITextRange::SetRange</a> sets both range ends simultaneously. The following example shows how to convert a nondegenerate range into a degenerate one (insertion point).

<code>range.End = range.Start</code>

Similarly, <code>range.Start = range.End</code> converts the range into an insertion point at the end position.

The following example adds 1 to the end position, if it is not at the end of the story.

<code>range.End = range.End + 1</code>

This also makes the end position the active end of the range, and it can turn a degenerate range into a nondegenerate one.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-getstart">GetStart</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-setend">SetEnd</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-setrange">SetRange</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>