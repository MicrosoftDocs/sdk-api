---
UID: NF:tom.ITextRow.Insert
title: ITextRow::Insert (tom.h)
description: Inserts a row, or rows, at the location identified by the associated ITextRange2 object.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","Insert method","ITextRow.Insert","ITextRow::Insert","Insert","Insert method [Windows Controls]","Insert method [Windows Controls]","ITextRow interface","controls.itextrow_insert","tom/ITextRow::Insert"]
old-location: controls\itextrow_insert.htm
tech.root: Controls
ms.assetid: b46a6391-7332-4cca-8199-d801a1e4c299
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],Insert method, ITextRow.Insert, ITextRow::Insert, Insert, Insert method [Windows Controls], Insert method [Windows Controls],ITextRow interface, controls.itextrow_insert, tom/ITextRow::Insert
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
 - ITextRow::Insert
 - tom/ITextRow::Insert
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
 - ITextRow.Insert
---

# ITextRow::Insert


## -description

Inserts a row, or rows, at the location identified by the associated <a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a> object.

## -parameters

### -param cRow [in]

Type: <b>long</b>

The number of rows to insert.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>