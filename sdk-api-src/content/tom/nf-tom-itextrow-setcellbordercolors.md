---
UID: NF:tom.ITextRow.SetCellBorderColors
title: ITextRow::SetCellBorderColors (tom.h)
description: Sets the border colors of the active cell.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetCellBorderColors method","ITextRow.SetCellBorderColors","ITextRow::SetCellBorderColors","SetCellBorderColors","SetCellBorderColors method [Windows Controls]","SetCellBorderColors method [Windows Controls]","ITextRow interface","controls.itextrow_setcellbordercolors","tom/ITextRow::SetCellBorderColors"]
old-location: controls\itextrow_setcellbordercolors.htm
tech.root: Controls
ms.assetid: 2a8762ba-a92b-46aa-99bc-57406a872174
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellBorderColors method, ITextRow.SetCellBorderColors, ITextRow::SetCellBorderColors, SetCellBorderColors, SetCellBorderColors method [Windows Controls], SetCellBorderColors method [Windows Controls],ITextRow interface, controls.itextrow_setcellbordercolors, tom/ITextRow::SetCellBorderColors
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
 - ITextRow::SetCellBorderColors
 - tom/ITextRow::SetCellBorderColors
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
 - ITextRow.SetCellBorderColors
---

# ITextRow::SetCellBorderColors


## -description

Sets the border colors of the active cell.

## -parameters

### -param crLeft [in]

Type: <b>long</b>

The left border color.

### -param crTop [in]

Type: <b>long</b>

The top border color.

### -param crRight [in]

Type: <b>long</b>

The right border color.

### -param crBottom [in]

Type: <b>long</b>

The bottom border color.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellbordercolors">ITextRow::GetCellBorderColors</a>