---
UID: NF:tom.ITextRow.SetCellShading
title: ITextRow::SetCellShading (tom.h)
description: Sets the shading of the active cell.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetCellShading method","ITextRow.SetCellShading","ITextRow::SetCellShading","SetCellShading","SetCellShading method [Windows Controls]","SetCellShading method [Windows Controls]","ITextRow interface","controls.itextrow_setcellshading","tom/ITextRow::SetCellShading"]
old-location: controls\itextrow_setcellshading.htm
tech.root: Controls
ms.assetid: 9163a9a3-6f8c-4318-a5a1-4b00a9037f6a
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellShading method, ITextRow.SetCellShading, ITextRow::SetCellShading, SetCellShading, SetCellShading method [Windows Controls], SetCellShading method [Windows Controls],ITextRow interface, controls.itextrow_setcellshading, tom/ITextRow::SetCellShading
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
 - ITextRow::SetCellShading
 - tom/ITextRow::SetCellShading
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
 - ITextRow.SetCellShading
---

# ITextRow::SetCellShading


## -description

Sets the shading of the active cell.

## -parameters

### -param Value [in]

Type: <b>long</b>

The shading of the active cell.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The shading is given in hundredths of a percent, so full shading is given by the value 10000. The shading percentage determines the mix of the cell foreground and background colors to be used for the cell background. A shading of 0 uses the cell background color alone. A shading of 10000 (100%) uses the foreground color alone. Values in between mix the foreground and background colors, weighting the background with (10000 – CellShading)/1000 and the foreground with CellShading/1000. These ratios are applied to the red, green, and blue channels independently of one another.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellshading">ITextRow::GetCellShading</a>