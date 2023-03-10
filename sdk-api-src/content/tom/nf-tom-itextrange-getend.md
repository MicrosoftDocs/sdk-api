---
UID: NF:tom.ITextRange.GetEnd
title: ITextRange::GetEnd (tom.h)
description: Gets the end character position of the range.
helpviewer_keywords: ["GetEnd","GetEnd method [Windows Controls]","GetEnd method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","GetEnd method","ITextRange.GetEnd","ITextRange::GetEnd","_win32_ITextRange_GetEnd","_win32_ITextRange_GetEnd_cpp","controls.ITextRange_GetEnd","controls._win32_ITextRange_GetEnd","tom/ITextRange::GetEnd"]
old-location: controls\ITextRange_GetEnd.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getend.htm
ms.date: 12/05/2018
ms.keywords: GetEnd, GetEnd method [Windows Controls], GetEnd method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetEnd method, ITextRange.GetEnd, ITextRange::GetEnd, _win32_ITextRange_GetEnd, _win32_ITextRange_GetEnd_cpp, controls.ITextRange_GetEnd, controls._win32_ITextRange_GetEnd, tom/ITextRange::GetEnd
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
 - ITextRange::GetEnd
 - tom/ITextRange::GetEnd
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
 - ITextRange.GetEnd
---

# ITextRange::GetEnd


## -description

Gets the end character position of the range.

## -parameters

### -param pcpLim

Type: <b>long*</b>

The end character position.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pcpLim</i> is null, the method fails and it returns E_INVALIDARG.

## -remarks

Although a pointer to a range remains valid when the text is edited, this is not the case for the 
				character position. A 
				character position is volatile; that is, it becomes invalid as soon as text is inserted or deleted before the 
				character position. Be careful about using methods that return 
				character position values, especially if the values are to be stored for any duration. 

This method is similar to the <a href="/windows/desktop/api/tom/nf-tom-itextrange-getstart">ITextRange::GetStart</a> method which gets the start character position of the range.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-getstart">GetStart</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/api/tom/nf-tom-itextrange-setend">SetEnd</a>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>