---
UID: NF:tom.ITextPara.CanChange
title: ITextPara::CanChange (tom.h)
description: Determines whether the paragraph formatting can be changed.
helpviewer_keywords: ["CanChange","CanChange method [Windows Controls]","CanChange method [Windows Controls]","ITextPara interface","ITextPara interface [Windows Controls]","CanChange method","ITextPara.CanChange","ITextPara::CanChange","_win32_ITextPara_CanChange","_win32_ITextPara_CanChange_cpp","controls.ITextPara_CanChange","controls._win32_ITextPara_CanChange","tom/ITextPara::CanChange"]
old-location: controls\ITextPara_CanChange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara\itextparacanchange.htm
ms.date: 12/05/2018
ms.keywords: CanChange, CanChange method [Windows Controls], CanChange method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],CanChange method, ITextPara.CanChange, ITextPara::CanChange, _win32_ITextPara_CanChange, _win32_ITextPara_CanChange_cpp, controls.ITextPara_CanChange, controls._win32_ITextPara_CanChange, tom/ITextPara::CanChange
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
 - ITextPara::CanChange
 - tom/ITextPara::CanChange
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
 - ITextPara.CanChange
---

# ITextPara::CanChange


## -description

Determines whether the paragraph formatting can be changed.

## -parameters

### -param pValue [retval]

Type: <b>long*</b>

A variable that is <b>tomTrue</b> if the paragraph formatting can be changed or <b>tomFalse</b> if it cannot be changed. This parameter can be null.

## -returns

Type: <b>HRESULT</b>

If paragraph formatting can change, <b>ITextPara::CanChange</b> succeeds and returns <b>S_OK</b>. If paragraph formatting cannot change, the method fails and returns S_FALSE. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -remarks

The *<i>pbCanChange</i>  parameter returns <b>tomTrue</b> only if the paragraph formatting can be changed (that is, if no part of an associated range is protected and an associated document is not read-only). If this <a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> object is a duplicate, no protection rules apply.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>