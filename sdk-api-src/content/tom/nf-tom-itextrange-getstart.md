---
UID: NF:tom.ITextRange.GetStart
title: ITextRange::GetStart (tom.h)
description: Gets the start character position of the range.
helpviewer_keywords: ["GetStart","GetStart method [Windows Controls]","GetStart method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","GetStart method","ITextRange.GetStart","ITextRange::GetStart","_win32_ITextRange_GetStart","_win32_ITextRange_GetStart_cpp","controls.ITextRange_GetStart","controls._win32_ITextRange_GetStart","tom/ITextRange::GetStart"]
old-location: controls\ITextRange_GetStart.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getstart.htm
ms.date: 12/05/2018
ms.keywords: GetStart, GetStart method [Windows Controls], GetStart method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetStart method, ITextRange.GetStart, ITextRange::GetStart, _win32_ITextRange_GetStart, _win32_ITextRange_GetStart_cpp, controls.ITextRange_GetStart, controls._win32_ITextRange_GetStart, tom/ITextRange::GetStart
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
 - ITextRange::GetStart
 - tom/ITextRange::GetStart
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
 - ITextRange.GetStart
---

# ITextRange::GetStart


## -description

Gets the start character position of the range.

## -parameters

### -param pcpFirst

Type: <b>long*</b>

The start character position.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pcpFirst</i> is null, the method fails and it returns E_INVALIDARG.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-getend">GetEnd</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-setstart">SetStart</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>