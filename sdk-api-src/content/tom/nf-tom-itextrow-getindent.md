---
UID: NF:tom.ITextRow.GetIndent
title: ITextRow::GetIndent (tom.h)
description: Gets the indent of this row.
helpviewer_keywords: ["GetIndent","GetIndent method [Windows Controls]","GetIndent method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetIndent method","ITextRow.GetIndent","ITextRow::GetIndent","controls.itextrow_getindent","tom/ITextRow::GetIndent"]
old-location: controls\itextrow_getindent.htm
tech.root: Controls
ms.assetid: 9caea02f-f8db-4366-aea6-d40759b8f792
ms.date: 12/05/2018
ms.keywords: GetIndent, GetIndent method [Windows Controls], GetIndent method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetIndent method, ITextRow.GetIndent, ITextRow::GetIndent, controls.itextrow_getindent, tom/ITextRow::GetIndent
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
 - ITextRow::GetIndent
 - tom/ITextRow::GetIndent
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
 - ITextRow.GetIndent
---

# ITextRow::GetIndent


## -description

Gets the indent of this row.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The indent of the row.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setindent">ITextRow::SetIndent</a>