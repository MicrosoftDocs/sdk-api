---
UID: NF:tom.ITextRange.GetFont
title: ITextRange::GetFont (tom.h)
description: Gets an ITextFont object with the character attributes of the specified range.
helpviewer_keywords: ["GetFont","GetFont method [Windows Controls]","GetFont method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","GetFont method","ITextRange.GetFont","ITextRange::GetFont","_win32_ITextRange_GetFont","_win32_ITextRange_GetFont_cpp","controls.ITextRange_GetFont","controls._win32_ITextRange_GetFont","tom/ITextRange::GetFont"]
old-location: controls\ITextRange_GetFont.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getfont.htm
ms.date: 12/05/2018
ms.keywords: GetFont, GetFont method [Windows Controls], GetFont method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetFont method, ITextRange.GetFont, ITextRange::GetFont, _win32_ITextRange_GetFont, _win32_ITextRange_GetFont_cpp, controls.ITextRange_GetFont, controls._win32_ITextRange_GetFont, tom/ITextRange::GetFont
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
 - ITextRange::GetFont
 - tom/ITextRange::GetFont
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
 - ITextRange.GetFont
---

# ITextRange::GetFont


## -description

Gets an <a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> object with the character attributes of the specified range.

## -parameters

### -param ppFont

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>**</b>

The pointer to an <a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> object.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>ppFont</i> is null, the method fails and it returns E_INVALIDARG.

## -remarks

For plain-text controls, these objects do not vary from range to range, but in rich-text solutions, they do. See the section on <a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a> for further details.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextfont">ITextFont</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>