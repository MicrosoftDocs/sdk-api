---
UID: NF:tom.ITextRow.GetCellBorderWidths
title: ITextRow::GetCellBorderWidths (tom.h)
description: Gets the border widths of the active cell.
helpviewer_keywords: ["GetCellBorderWidths","GetCellBorderWidths method [Windows Controls]","GetCellBorderWidths method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetCellBorderWidths method","ITextRow.GetCellBorderWidths","ITextRow::GetCellBorderWidths","controls.itextrow_getcellborderwidths","tom/ITextRow::GetCellBorderWidths"]
old-location: controls\itextrow_getcellborderwidths.htm
tech.root: Controls
ms.assetid: e0ab26ca-ffb6-4f75-846b-e267e4ad6572
ms.date: 12/05/2018
ms.keywords: GetCellBorderWidths, GetCellBorderWidths method [Windows Controls], GetCellBorderWidths method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellBorderWidths method, ITextRow.GetCellBorderWidths, ITextRow::GetCellBorderWidths, controls.itextrow_getcellborderwidths, tom/ITextRow::GetCellBorderWidths
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
 - ITextRow::GetCellBorderWidths
 - tom/ITextRow::GetCellBorderWidths
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
 - ITextRow.GetCellBorderWidths
---

# ITextRow::GetCellBorderWidths


## -description

Gets the border widths of the active cell.

## -parameters

### -param pduLeft [in]

Type: <b>long*</b>

The active-cell left border width.

### -param pduTop [in]

Type: <b>long*</b>

The active-cell top border width.

### -param pduRight [in]

Type: <b>long*</b>

The active-cell right border width.

### -param pduBottom [in]

Type: <b>long*</b>

The active-cell bottom border width.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellborderwidths">ITextRow::SetCellBorderWidths</a>