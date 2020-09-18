---
UID: NF:tom.ITextPara.IsEqual
title: ITextPara::IsEqual (tom.h)
description: Determines if the current range has the same properties as a specified range.
helpviewer_keywords: ["ITextPara interface [Windows Controls]","IsEqual method","ITextPara.IsEqual","ITextPara::IsEqual","IsEqual","IsEqual method [Windows Controls]","IsEqual method [Windows Controls]","ITextPara interface","_win32_ITextPara_IsEqual","_win32_ITextPara_IsEqual_cpp","controls.ITextPara_IsEqual","controls._win32_ITextPara_IsEqual","tom/ITextPara::IsEqual"]
old-location: controls\ITextPara_IsEqual.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\itextpara\itextparaisequal.htm
ms.date: 12/05/2018
ms.keywords: ITextPara interface [Windows Controls],IsEqual method, ITextPara.IsEqual, ITextPara::IsEqual, IsEqual, IsEqual method [Windows Controls], IsEqual method [Windows Controls],ITextPara interface, _win32_ITextPara_IsEqual, _win32_ITextPara_IsEqual_cpp, controls.ITextPara_IsEqual, controls._win32_ITextPara_IsEqual, tom/ITextPara::IsEqual
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
 - ITextPara::IsEqual
 - tom/ITextPara::IsEqual
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
 - ITextPara.IsEqual
---

# ITextPara::IsEqual


## -description

Determines if the current range has the same properties as a specified range.

## -parameters

### -param pPara

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>*</b>

The <a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a> range that is compared to the current range.

### -param pValue

Type: <b>long*</b>

The comparison result. The value can be null.

## -returns

Type: <b>HRESULT</b>

If the objects are equal, <b>ITextPara::IsEqual</b> succeeds and returns <b>S_OK</b>. If the objects are not equal, the method fails and returns S_FALSE. For more information about COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/tom/nn-tom-itextpara">ITextPara</a>



<b>Reference</b>



<a href="/windows/desktop/Controls/text-object-model">Text Object Model</a>