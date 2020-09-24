---
UID: NF:tom.ITextRow.GetCellBorderColors
title: ITextRow::GetCellBorderColors (tom.h)
description: Gets the border colors of the active cell.
helpviewer_keywords: ["GetCellBorderColors","GetCellBorderColors method [Windows Controls]","GetCellBorderColors method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetCellBorderColors method","ITextRow.GetCellBorderColors","ITextRow::GetCellBorderColors","controls.itextrow_getcellbordercolors","tom/ITextRow::GetCellBorderColors"]
old-location: controls\itextrow_getcellbordercolors.htm
tech.root: Controls
ms.assetid: 2cc0a3b0-3988-4dff-9553-a86d37f4011f
ms.date: 12/05/2018
ms.keywords: GetCellBorderColors, GetCellBorderColors method [Windows Controls], GetCellBorderColors method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellBorderColors method, ITextRow.GetCellBorderColors, ITextRow::GetCellBorderColors, controls.itextrow_getcellbordercolors, tom/ITextRow::GetCellBorderColors
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
 - ITextRow::GetCellBorderColors
 - tom/ITextRow::GetCellBorderColors
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
 - ITextRow.GetCellBorderColors
---

# ITextRow::GetCellBorderColors


## -description

Gets the border colors of the active cell.

## -parameters

### -param pcrLeft [in]

Type: <b>long*</b>

The active-cell left border color.

### -param pcrTop [in]

Type: <b>long*</b>

The active-cell top border color.

### -param pcrRight [in]

Type: <b>long*</b>

The active-cell right border color.

### -param pcrBottom [in]

Type: <b>long*</b>

The active-cell bottom border color.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellbordercolors">ITextRow::SetCellBorderColors</a>