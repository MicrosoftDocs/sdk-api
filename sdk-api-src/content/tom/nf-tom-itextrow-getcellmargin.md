---
UID: NF:tom.ITextRow.GetCellMargin
title: ITextRow::GetCellMargin (tom.h)
description: Gets the cell margin of this row.
helpviewer_keywords: ["GetCellMargin","GetCellMargin method [Windows Controls]","GetCellMargin method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetCellMargin method","ITextRow.GetCellMargin","ITextRow::GetCellMargin","controls.itextrow_getcellmargin","tom/ITextRow::GetCellMargin"]
old-location: controls\itextrow_getcellmargin.htm
tech.root: Controls
ms.assetid: fc477a0f-2368-40c8-9b75-caec3afedea0
ms.date: 12/05/2018
ms.keywords: GetCellMargin, GetCellMargin method [Windows Controls], GetCellMargin method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellMargin method, ITextRow.GetCellMargin, ITextRow::GetCellMargin, controls.itextrow_getcellmargin, tom/ITextRow::GetCellMargin
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
 - ITextRow::GetCellMargin
 - tom/ITextRow::GetCellMargin
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
 - ITextRow.GetCellMargin
---

# ITextRow::GetCellMargin


## -description

Gets the cell margin of this row.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The cell margin.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellmargin">ITextRow::SetCellMargin</a>