---
UID: NF:tom.ITextRow.SetCellWidth
title: ITextRow::SetCellWidth (tom.h)
description: Sets the active cell width in twips.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetCellWidth method","ITextRow.SetCellWidth","ITextRow::SetCellWidth","SetCellWidth","SetCellWidth method [Windows Controls]","SetCellWidth method [Windows Controls]","ITextRow interface","controls.itextrow_setcellwidth","tom/ITextRow::SetCellWidth"]
old-location: controls\itextrow_setcellwidth.htm
tech.root: Controls
ms.assetid: 321c5255-9cd5-46ea-a592-165d288bc452
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellWidth method, ITextRow.SetCellWidth, ITextRow::SetCellWidth, SetCellWidth, SetCellWidth method [Windows Controls], SetCellWidth method [Windows Controls],ITextRow interface, controls.itextrow_setcellwidth, tom/ITextRow::SetCellWidth
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
 - ITextRow::SetCellWidth
 - tom/ITextRow::SetCellWidth
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
 - ITextRow.SetCellWidth
---

# ITextRow::SetCellWidth


## -description

Sets the active cell width in twips.

## -parameters

### -param Value [in]

Type: <b>long</b>

The width of the active cell.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The total width of the entire row must be less than 22 inches, or 1440×22.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellwidth">ITextRow::GetCellWidth</a>