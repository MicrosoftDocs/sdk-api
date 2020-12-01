---
UID: NF:tom.ITextRow.GetCellWidth
title: ITextRow::GetCellWidth (tom.h)
description: Gets the width of the active cell.
helpviewer_keywords: ["GetCellWidth","GetCellWidth method [Windows Controls]","GetCellWidth method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetCellWidth method","ITextRow.GetCellWidth","ITextRow::GetCellWidth","controls.itextrow_getcellwidth","tom/ITextRow::GetCellWidth"]
old-location: controls\itextrow_getcellwidth.htm
tech.root: Controls
ms.assetid: dc73fdf4-29ce-4432-825d-725d61717b7a
ms.date: 12/05/2018
ms.keywords: GetCellWidth, GetCellWidth method [Windows Controls], GetCellWidth method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellWidth method, ITextRow.GetCellWidth, ITextRow::GetCellWidth, controls.itextrow_getcellwidth, tom/ITextRow::GetCellWidth
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
 - ITextRow::GetCellWidth
 - tom/ITextRow::GetCellWidth
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
 - ITextRow.GetCellWidth
---

# ITextRow::GetCellWidth


## -description

Gets the width of the active cell.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The width of the active cell, in twips.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The width of the cell, and/or the entire row, must be less than 22 inches (1440 x 22).

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellwidth">ITextRow::SetCellWidth</a>