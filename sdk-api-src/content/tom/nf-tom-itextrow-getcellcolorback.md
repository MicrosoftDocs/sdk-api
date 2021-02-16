---
UID: NF:tom.ITextRow.GetCellColorBack
title: ITextRow::GetCellColorBack (tom.h)
description: Gets the background color of the active cell.
helpviewer_keywords: ["GetCellColorBack","GetCellColorBack method [Windows Controls]","GetCellColorBack method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetCellColorBack method","ITextRow.GetCellColorBack","ITextRow::GetCellColorBack","controls.itextrow_getcellcolorback","tom/ITextRow::GetCellColorBack"]
old-location: controls\itextrow_getcellcolorback.htm
tech.root: Controls
ms.assetid: d199c4d7-17fd-4d1d-9d6d-b11db71f1363
ms.date: 12/05/2018
ms.keywords: GetCellColorBack, GetCellColorBack method [Windows Controls], GetCellColorBack method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellColorBack method, ITextRow.GetCellColorBack, ITextRow::GetCellColorBack, controls.itextrow_getcellcolorback, tom/ITextRow::GetCellColorBack
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
 - ITextRow::GetCellColorBack
 - tom/ITextRow::GetCellColorBack
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
 - ITextRow.GetCellColorBack
---

# ITextRow::GetCellColorBack


## -description

Gets the background color of the active cell.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The background color.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellcolorback">ITextRow::SetCellColorBack</a>