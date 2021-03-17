---
UID: NF:tom.ITextRow.SetCellIndex
title: ITextRow::SetCellIndex (tom.h)
description: Sets the index of the active cell.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetCellIndex method","ITextRow.SetCellIndex","ITextRow::SetCellIndex","SetCellIndex","SetCellIndex method [Windows Controls]","SetCellIndex method [Windows Controls]","ITextRow interface","controls.itextrow_setcellindex","tom/ITextRow::SetCellIndex"]
old-location: controls\itextrow_setcellindex.htm
tech.root: Controls
ms.assetid: 4b31ed10-f153-4614-ba96-95271fe4b218
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellIndex method, ITextRow.SetCellIndex, ITextRow::SetCellIndex, SetCellIndex, SetCellIndex method [Windows Controls], SetCellIndex method [Windows Controls],ITextRow interface, controls.itextrow_setcellindex, tom/ITextRow::SetCellIndex
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
 - ITextRow::SetCellIndex
 - tom/ITextRow::SetCellIndex
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
 - ITextRow.SetCellIndex
---

# ITextRow::SetCellIndex


## -description

Sets the index of the active cell.

## -parameters

### -param Value [in]

Type: <b>long</b>

The cell index.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

You can get or set parameters for an active cell.

 If the cell index is greater than the cell count, and the cell index is less that 63 (the maximum cell count), then the cell count is increased to cell index + 1.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellcount">ITextRow::GetCellCount</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellindex">ITextRow::GetCellIndex</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellcount">ITextRow::SetCellCount</a>