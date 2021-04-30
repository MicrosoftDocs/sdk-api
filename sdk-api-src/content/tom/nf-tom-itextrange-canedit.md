---
UID: NF:tom.ITextRange.CanEdit
title: ITextRange::CanEdit (tom.h)
description: Determines whether the specified range can be edited.
helpviewer_keywords: ["CanEdit","CanEdit method [Windows Controls]","CanEdit method [Windows Controls]","ITextRange interface","ITextRange interface [Windows Controls]","CanEdit method","ITextRange.CanEdit","ITextRange::CanEdit","_win32_ITextRange_CanEdit","_win32_ITextRange_CanEdit_cpp","controls.ITextRange_CanEdit","controls._win32_ITextRange_CanEdit","tom/ITextRange::CanEdit"]
old-location: controls\ITextRange_CanEdit.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\canedit.htm
ms.date: 12/05/2018
ms.keywords: CanEdit, CanEdit method [Windows Controls], CanEdit method [Windows Controls],ITextRange interface, ITextRange interface [Windows Controls],CanEdit method, ITextRange.CanEdit, ITextRange::CanEdit, _win32_ITextRange_CanEdit, _win32_ITextRange_CanEdit_cpp, controls.ITextRange_CanEdit, controls._win32_ITextRange_CanEdit, tom/ITextRange::CanEdit
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
 - ITextRange::CanEdit
 - tom/ITextRange::CanEdit
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
 - ITextRange.CanEdit
---

# ITextRange::CanEdit


## -description

Determines whether the specified range can be edited.

## -parameters

### -param pValue [retval]

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> value indicating whether the range can be edited. It is <b>tomTrue</b> only if the specified range can be edited. The pointer can be null.

## -returns

Type: <b>HRESULT</b>

If the range can be edited, the method succeeds and returns <b>S_OK</b>. If the range cannot be edited, the method fails and returns <b>S_FALSE</b>. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -remarks

The range cannot be edited if any part of it is protected or if the document is read-only.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextrange">ITextRange</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>