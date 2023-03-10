---
UID: NF:tom.ITextRange.SetEnd
title: ITextRange::SetEnd (tom.h)
description: Sets the end position of the range.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","SetEnd method","ITextRange.SetEnd","ITextRange::SetEnd","SetEnd","SetEnd method [Windows Controls]","SetEnd method [Windows Controls]","ITextRange interface","_win32_ITextRange_SetEnd","_win32_ITextRange_SetEnd_cpp","controls.ITextRange_SetEnd","controls._win32_ITextRange_SetEnd","tom/ITextRange::SetEnd"]
old-location: controls\ITextRange_SetEnd.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setend.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],SetEnd method, ITextRange.SetEnd, ITextRange::SetEnd, SetEnd, SetEnd method [Windows Controls], SetEnd method [Windows Controls],ITextRange interface, _win32_ITextRange_SetEnd, _win32_ITextRange_SetEnd_cpp, controls.ITextRange_SetEnd, controls._win32_ITextRange_SetEnd, tom/ITextRange::SetEnd
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
 - ITextRange::SetEnd
 - tom/ITextRange::SetEnd
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
 - ITextRange.SetEnd
---

# ITextRange::SetEnd


## -description

Sets the end position of the range.

## -parameters

### -param cpLim

Type: <b>long</b>

The new end position.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE.

## -remarks

If the new end position is less than the start position, this method also sets the start position to  <i>cp</i>; that is, the range becomes an insertion point.

If this range is actually the selection, the end position becomes the active end and, if the display is not frozen, it is scrolled into view.


<a href="/windows/desktop/api/tom/nf-tom-itextrange-setstart">ITextRange::SetStart</a> sets the range's start position and <a href="/windows/desktop/api/tom/nf-tom-itextrange-setrange">ITextRange::SetRange</a> sets both range ends simultaneously. To convert a nondegenerate range, r, into a degenerate one (insertion point) at  the start position, use

<code>r.End = r.Start</code>

Similarly, r.Start = r.End converts r into an insertion point at the end position.

To add 1 to the end position, unless it is at the end of the story, use:

<code>r.End = r.End + 1</code>

This also makes end position the active end, and it can turn a degenerate range into a nondegenerate one.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-getend">GetEnd</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-setrange">SetRange</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-setstart">SetStart</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>