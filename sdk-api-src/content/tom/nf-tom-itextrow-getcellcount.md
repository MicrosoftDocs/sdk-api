---
UID: NF:tom.ITextRow.GetCellCount
title: ITextRow::GetCellCount (tom.h)
description: Gets the count of cells in this row.
helpviewer_keywords: ["GetCellCount","GetCellCount method [Windows Controls]","GetCellCount method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetCellCount method","ITextRow.GetCellCount","ITextRow::GetCellCount","controls.itextrow_getcellcount","tom/ITextRow::GetCellCount"]
old-location: controls\itextrow_getcellcount.htm
tech.root: Controls
ms.assetid: 4aae4fe5-5a54-4f32-9f89-01752701c871
ms.date: 12/05/2018
ms.keywords: GetCellCount, GetCellCount method [Windows Controls], GetCellCount method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellCount method, ITextRow.GetCellCount, ITextRow::GetCellCount, controls.itextrow_getcellcount, tom/ITextRow::GetCellCount
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
 - ITextRow::GetCellCount
 - tom/ITextRow::GetCellCount
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
 - ITextRow.GetCellCount
---

# ITextRow::GetCellCount


## -description

Gets the count of cells in this row.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The cell count for this row.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellcount">ITextRow::SetCellCount</a>