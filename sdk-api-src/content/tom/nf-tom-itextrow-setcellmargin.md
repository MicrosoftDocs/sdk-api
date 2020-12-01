---
UID: NF:tom.ITextRow.SetCellMargin
title: ITextRow::SetCellMargin (tom.h)
description: Sets the cell margin of a row.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetCellMargin method","ITextRow.SetCellMargin","ITextRow::SetCellMargin","SetCellMargin","SetCellMargin method [Windows Controls]","SetCellMargin method [Windows Controls]","ITextRow interface","controls.itextrow_setcellmargin","tom/ITextRow::SetCellMargin"]
old-location: controls\itextrow_setcellmargin.htm
tech.root: Controls
ms.assetid: 826be963-ccac-4bb3-b5e0-1df5554e1c8c
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellMargin method, ITextRow.SetCellMargin, ITextRow::SetCellMargin, SetCellMargin, SetCellMargin method [Windows Controls], SetCellMargin method [Windows Controls],ITextRow interface, controls.itextrow_setcellmargin, tom/ITextRow::SetCellMargin
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
 - ITextRow::SetCellMargin
 - tom/ITextRow::SetCellMargin
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
 - ITextRow.SetCellMargin
---

# ITextRow::SetCellMargin


## -description

Sets the cell margin of a row.

## -parameters

### -param Value [in]

Type: <b>long</b>

The cell margin. The cell margin is used for all cells in the row and is typically about 108 twips or 0.075 inches.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellmargin">ITextRow::GetCellMargin</a>