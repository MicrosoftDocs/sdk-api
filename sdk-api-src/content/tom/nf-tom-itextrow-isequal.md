---
UID: NF:tom.ITextRow.IsEqual
title: ITextRow::IsEqual (tom.h)
description: Compares two table rows to determine if they have the same properties.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","IsEqual method","ITextRow.IsEqual","ITextRow::IsEqual","IsEqual","IsEqual method [Windows Controls]","IsEqual method [Windows Controls]","ITextRow interface","controls.itextrow_isequal","tom/ITextRow::IsEqual"]
old-location: controls\itextrow_isequal.htm
tech.root: Controls
ms.assetid: 2e516a4d-0f3b-475b-969d-661662bfaeef
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],IsEqual method, ITextRow.IsEqual, ITextRow::IsEqual, IsEqual, IsEqual method [Windows Controls], IsEqual method [Windows Controls],ITextRow interface, controls.itextrow_isequal, tom/ITextRow::IsEqual
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - ITextRow::IsEqual
 - tom/ITextRow::IsEqual
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
 - ITextRow.IsEqual
---

# ITextRow::IsEqual


## -description

Compares two table rows to determine if they have the same properties.

## -parameters

### -param pRow [in]

Type: <b><a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>*</b>

The row to compare to.

### -param pB [out, retval]

Type: <b>long*</b>

 The comparison result. The value is set to  <b>tomTrue</b> if equal, and <b>tomFalse</b> if not. The value can be <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>