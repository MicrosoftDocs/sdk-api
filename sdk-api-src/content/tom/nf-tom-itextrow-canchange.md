---
UID: NF:tom.ITextRow.CanChange
title: ITextRow::CanChange (tom.h)
description: Determines whether changes can be made to this row.
helpviewer_keywords: ["CanChange","CanChange method [Windows Controls]","CanChange method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","CanChange method","ITextRow.CanChange","ITextRow::CanChange","controls.itextrow_canchange","tom/ITextRow::CanChange"]
old-location: controls\itextrow_canchange.htm
tech.root: Controls
ms.assetid: 721f3841-a50b-4569-b988-71a9fb96f16f
ms.date: 12/05/2018
ms.keywords: CanChange, CanChange method [Windows Controls], CanChange method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],CanChange method, ITextRow.CanChange, ITextRow::CanChange, controls.itextrow_canchange, tom/ITextRow::CanChange
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
 - ITextRow::CanChange
 - tom/ITextRow::CanChange
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
 - ITextRow.CanChange
---

# ITextRow::CanChange


## -description

Determines whether changes can be made to this row.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

A <a href="/windows/desktop/Controls/about-text-object-model">tomBool</a> indicating whether the row can be edited. It is <b>tomTrue</b> only if the row can be edited. The <i>pB</i> parameter can be <b>NULL</b>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The row can be changed only if no part of an associated range is protected and the associated document isn't read only.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>