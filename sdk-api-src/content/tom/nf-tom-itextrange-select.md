---
UID: NF:tom.ITextRange.Select
title: ITextRange::Select (tom.h)
description: Sets the start and end positions, and story values of the active selection, to those of this range.
helpviewer_keywords: ["ITextRange interface [Windows Controls]","Select method","ITextRange.Select","ITextRange::Select","Select","Select method [Windows Controls]","Select method [Windows Controls]","ITextRange interface","_win32_ITextRange_Select","_win32_ITextRange_Select_cpp","controls.ITextRange_Select","controls._win32_ITextRange_Select","tom/ITextRange::Select"]
old-location: controls\ITextRange_Select.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\select.htm
ms.date: 12/05/2018
ms.keywords: ITextRange interface [Windows Controls],Select method, ITextRange.Select, ITextRange::Select, Select, Select method [Windows Controls], Select method [Windows Controls],ITextRange interface, _win32_ITextRange_Select, _win32_ITextRange_Select_cpp, controls.ITextRange_Select, controls._win32_ITextRange_Select, tom/ITextRange::Select
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
 - ITextRange::Select
 - tom/ITextRange::Select
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
 - ITextRange.Select
---

# ITextRange::Select


## -description

Sets the start and end positions, and story values of the active selection, to those of this range.



## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b> value. If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns S_FALSE.

## -remarks

The active end of the new selection is at the end position. 

The caret for an ambiguous character position is displayed at the beginning of the line.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>
