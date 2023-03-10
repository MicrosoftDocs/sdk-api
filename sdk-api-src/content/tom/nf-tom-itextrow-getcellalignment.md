---
UID: NF:tom.ITextRow.GetCellAlignment
title: ITextRow::GetCellAlignment (tom.h)
description: Gets the vertical alignment of the active cell.
helpviewer_keywords: ["GetCellAlignment","GetCellAlignment method [Windows Controls]","GetCellAlignment method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetCellAlignment method","ITextRow.GetCellAlignment","ITextRow::GetCellAlignment","controls.itextrow_getcellalignment","tom/ITextRow::GetCellAlignment"]
old-location: controls\itextrow_getcellalignment.htm
tech.root: Controls
ms.assetid: 379d6fa5-ea73-4b72-9251-942f66925d8a
ms.date: 12/05/2018
ms.keywords: GetCellAlignment, GetCellAlignment method [Windows Controls], GetCellAlignment method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellAlignment method, ITextRow.GetCellAlignment, ITextRow::GetCellAlignment, controls.itextrow_getcellalignment, tom/ITextRow::GetCellAlignment
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
 - ITextRow::GetCellAlignment
 - tom/ITextRow::GetCellAlignment
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
 - ITextRow.GetCellAlignment
---

# ITextRow::GetCellAlignment


## -description

Gets the vertical alignment of the active cell.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The vertical alignment.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellalignment">ITextRow::SetCellAlignment</a>