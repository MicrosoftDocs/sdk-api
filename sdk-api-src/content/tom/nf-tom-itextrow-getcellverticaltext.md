---
UID: NF:tom.ITextRow.GetCellVerticalText
title: ITextRow::GetCellVerticalText (tom.h)
description: Gets the vertical-text setting of the active cell.
helpviewer_keywords: ["GetCellVerticalText","GetCellVerticalText method [Windows Controls]","GetCellVerticalText method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetCellVerticalText method","ITextRow.GetCellVerticalText","ITextRow::GetCellVerticalText","controls.itextrow_getcellverticaltext","tom/ITextRow::GetCellVerticalText"]
old-location: controls\itextrow_getcellverticaltext.htm
tech.root: Controls
ms.assetid: 3c94a4af-0212-4422-bee2-7a9148a40b28
ms.date: 12/05/2018
ms.keywords: GetCellVerticalText, GetCellVerticalText method [Windows Controls], GetCellVerticalText method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetCellVerticalText method, ITextRow.GetCellVerticalText, ITextRow::GetCellVerticalText, controls.itextrow_getcellverticaltext, tom/ITextRow::GetCellVerticalText
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
 - ITextRow::GetCellVerticalText
 - tom/ITextRow::GetCellVerticalText
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
 - ITextRow.GetCellVerticalText
---

# ITextRow::GetCellVerticalText


## -description

Gets the vertical-text setting of the active cell.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The vertical-text setting

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setcellverticaltext">ITextRow::SetCellVerticalText</a>