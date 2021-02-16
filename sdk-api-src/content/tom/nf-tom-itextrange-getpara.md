---
UID: NF:tom.ITextRange.GetPara
title: ITextRange::GetPara (tom.h)
description: Gets an ITextPara object with the paragraph attributes of the specified range.
helpviewer_keywords: ["GetPara","GetPara method [Windows Controls]","GetPara method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","GetPara method","ITextRange.GetPara","ITextRange::GetPara","_win32_ITextRange_GetPara","_win32_ITextRange_GetPara_cpp","controls.ITextRange_GetPara","controls._win32_ITextRange_GetPara","tom/ITextRange::GetPara"]
old-location: controls\ITextRange_GetPara.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getpara.htm
ms.date: 12/05/2018
ms.keywords: GetPara, GetPara method [Windows Controls], GetPara method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetPara method, ITextRange.GetPara, ITextRange::GetPara, _win32_ITextRange_GetPara, _win32_ITextRange_GetPara_cpp, controls.ITextRange_GetPara, controls._win32_ITextRange_GetPara, tom/ITextRange::GetPara
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
 - ITextRange::GetPara
 - tom/ITextRange::GetPara
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
 - ITextRange.GetPara
---

# ITextRange::GetPara


## -description

Gets an <a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> object with the paragraph attributes of the specified range.

## -parameters

### -param ppPara

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>**</b>

The pointer to the <a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> object.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>ppPara</i> is null, the method fails and it returns E_INVALIDARG.

## -remarks

For plain-text controls, these objects do not vary from range to range, but in rich-text solutions, they do. See the section on <a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> for further details.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>