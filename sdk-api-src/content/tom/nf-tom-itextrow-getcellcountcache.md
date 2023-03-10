---
UID: NF:tom.ITextRow.GetCellCountCache
title: ITextRow::GetCellCountCache (tom.h)
description: Gets the count of cells cached for this row.
helpviewer_keywords: ["GetCellCountCache","GetCellCountCache method [Windows Controls]","GetCellCountCache method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetCellCountCache method","ITextRow.GetCellCountCache","ITextRow::GetCellCountCache","controls.itextrow_getcellcountcache","tom/ITextRow::GetCellCountCache"]
old-location: controls\itextrow_getcellcountcache.htm
tech.root: Controls
ms.assetid: e94abbcb-2a7a-4904-a832-0d2158d49010
ms.date: 12/05/2018
ms.keywords: GetCellCountCache, GetCellCountCache method [Windows Controls], GetCellCountCache method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellCountCache method, ITextRow.GetCellCountCache, ITextRow::GetCellCountCache, controls.itextrow_getcellcountcache, tom/ITextRow::GetCellCountCache
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
 - ITextRow::GetCellCountCache
 - tom/ITextRow::GetCellCountCache
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
 - ITextRow.GetCellCountCache
---

# ITextRow::GetCellCountCache


## -description

Gets the count of cells cached for this row.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The cached cell count.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If all cells are identical, properties need to be cached only for the cell with index 0. If the cached count is less than the cell count, the cell parameters for index CellCountCache – 1 are used for cells with larger indices.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellcountcache">ITextRow::SetCellCountCache</a>