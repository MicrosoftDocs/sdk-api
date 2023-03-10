---
UID: NF:tom.ITextRow.SetCellCountCache
title: ITextRow::SetCellCountCache (tom.h)
description: Sets the count of cells cached for a row.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetCellCountCache method","ITextRow.SetCellCountCache","ITextRow::SetCellCountCache","SetCellCountCache","SetCellCountCache method [Windows Controls]","SetCellCountCache method [Windows Controls]","ITextRow interface","controls.itextrow_setcellcountcache","tom/ITextRow::SetCellCountCache"]
old-location: controls\itextrow_setcellcountcache.htm
tech.root: Controls
ms.assetid: 54b9a0a0-1822-4cd6-afef-8ed9403e750a
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellCountCache method, ITextRow.SetCellCountCache, ITextRow::SetCellCountCache, SetCellCountCache, SetCellCountCache method [Windows Controls], SetCellCountCache method [Windows Controls],ITextRow interface, controls.itextrow_setcellcountcache, tom/ITextRow::SetCellCountCache
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
 - ITextRow::SetCellCountCache
 - tom/ITextRow::SetCellCountCache
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
 - ITextRow.SetCellCountCache
---

# ITextRow::SetCellCountCache


## -description

Sets the count of cells cached for a row.

## -parameters

### -param Value [in]

Type: <b>long</b>

The cell count.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If all cells are identical, properties need to be cached only for the cell with index 0. If the cached count is less than the cell count, the cell parameters for index CellCountCache – 1 are used for cells with larger indices.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellcountcache">ITextRow::GetCellCountCache</a>