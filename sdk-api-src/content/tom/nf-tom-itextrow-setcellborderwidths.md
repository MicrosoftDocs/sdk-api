---
UID: NF:tom.ITextRow.SetCellBorderWidths
title: ITextRow::SetCellBorderWidths (tom.h)
description: Sets the border widths of the active cell.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetCellBorderWidths method","ITextRow.SetCellBorderWidths","ITextRow::SetCellBorderWidths","SetCellBorderWidths","SetCellBorderWidths method [Windows Controls]","SetCellBorderWidths method [Windows Controls]","ITextRow interface","controls.itextrow_setcellborderwidths","tom/ITextRow::SetCellBorderWidths"]
old-location: controls\itextrow_setcellborderwidths.htm
tech.root: Controls
ms.assetid: 343270e6-8f92-4429-9350-4031ae8bb0e0
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellBorderWidths method, ITextRow.SetCellBorderWidths, ITextRow::SetCellBorderWidths, SetCellBorderWidths, SetCellBorderWidths method [Windows Controls], SetCellBorderWidths method [Windows Controls],ITextRow interface, controls.itextrow_setcellborderwidths, tom/ITextRow::SetCellBorderWidths
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
 - ITextRow::SetCellBorderWidths
 - tom/ITextRow::SetCellBorderWidths
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
 - ITextRow.SetCellBorderWidths
---

# ITextRow::SetCellBorderWidths


## -description

Sets the border widths of the active cell.

## -parameters

### -param duLeft [in]

Type: <b>long</b>

The left border width.

### -param duTop [in]

Type: <b>long</b>

The top border width.

### -param duRight [in]

Type: <b>long</b>

The right border width.

### -param duBottom [in]

Type: <b>long</b>

The bottom border width.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellborderwidths">ITextRow::GetCellBorderWidths</a>