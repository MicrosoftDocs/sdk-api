---
UID: NF:tom.ITextRange.GetStoryLength
title: ITextRange::GetStoryLength (tom.h)
description: Gets the count of characters in the range's story.
helpviewer_keywords: ["GetStoryLength","GetStoryLength method [Windows Controls]","GetStoryLength method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","GetStoryLength method","ITextRange.GetStoryLength","ITextRange::GetStoryLength","_win32_ITextRange_GetStoryLength","_win32_ITextRange_GetStoryLength_cpp","controls.ITextRange_GetStoryLength","controls._win32_ITextRange_GetStoryLength","tom/ITextRange::GetStoryLength"]
old-location: controls\ITextRange_GetStoryLength.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\getstorylength.htm
ms.date: 12/05/2018
ms.keywords: GetStoryLength, GetStoryLength method [Windows Controls], GetStoryLength method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],GetStoryLength method, ITextRange.GetStoryLength, ITextRange::GetStoryLength, _win32_ITextRange_GetStoryLength, _win32_ITextRange_GetStoryLength_cpp, controls.ITextRange_GetStoryLength, controls._win32_ITextRange_GetStoryLength, tom/ITextRange::GetStoryLength
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
 - ITextRange::GetStoryLength
 - tom/ITextRange::GetStoryLength
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
 - ITextRange.GetStoryLength
---

# ITextRange::GetStoryLength


## -description

Gets the count of characters in the range's story.

## -parameters

### -param pCount

Type: <b>long*</b>

The count of characters in the range's story.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If <i>pCount</i> is null, the method fails and it returns E_INVALIDARG.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>