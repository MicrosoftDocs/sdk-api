---
UID: NF:tom.ITextRange.SetRange
title: ITextRange::SetRange (tom.h)
description: Adjusts the range endpoints to the specified values.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","SetRange method","ITextRange.SetRange","ITextRange::SetRange","SetRange","SetRange method [Windows Controls]","SetRange method [Windows Controls]","ITextRange interface","_win32_ITextRange_SetRange","_win32_ITextRange_SetRange_cpp","controls.ITextRange_SetRange","controls._win32_ITextRange_SetRange","tom/ITextRange::SetRange"]
old-location: controls\ITextRange_SetRange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\setrange.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],SetRange method, ITextRange.SetRange, ITextRange::SetRange, SetRange, SetRange method [Windows Controls], SetRange method [Windows Controls],ITextRange interface, _win32_ITextRange_SetRange, _win32_ITextRange_SetRange_cpp, controls.ITextRange_SetRange, controls._win32_ITextRange_SetRange, tom/ITextRange::SetRange
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
 - ITextRange::SetRange
 - tom/ITextRange::SetRange
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
 - ITextRange.SetRange
---

# ITextRange::SetRange


## -description

Adjusts the range endpoints to the specified values.

## -parameters

### -param cpAnchor

Type: <b>long</b>

The character position for the anchor end of the range.

### -param cpActive

Type: <b>long</b>

The character position for the active end of the range.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method sets the range's start position to <code>min(cpActive, cpAnchor)</code>, and the end position to <code>max(cpActive, cpAnchor)</code>. If the range is a nondegenerate selection, <i>cpAnchor</i> is the active end, and <i>cpAnchor</i> is the anchor end.  If the range is a degenerate selection, the selection is displayed at the start of the line, rather than at the end of the previous line.

This method removes any other subranges this range may have. To preserve the current subranges, use <a href="/windows/desktop/api/tom/nf-tom-itextrange2-setactivesubrange">ITextRange2::SetActiveSubrange</a>. 


If the text range is a selection, you can set the attributes of the selection by using the <a href="/windows/desktop/api/tom/nf-tom-itextselection-setflags">ITextSelection::SetFlags</a> method.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>