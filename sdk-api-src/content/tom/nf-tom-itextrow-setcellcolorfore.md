---
UID: NF:tom.ITextRow.SetCellColorFore
title: ITextRow::SetCellColorFore (tom.h)
description: Sets the foreground color of the active cell.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetCellColorFore method","ITextRow.SetCellColorFore","ITextRow::SetCellColorFore","SetCellColorFore","SetCellColorFore method [Windows Controls]","SetCellColorFore method [Windows Controls]","ITextRow interface","controls.itextrow_setcellcolorfore","tom/ITextRow::SetCellColorFore"]
old-location: controls\itextrow_setcellcolorfore.htm
tech.root: Controls
ms.assetid: 2eff9f39-b79d-4fcb-b8ee-ef067cff2c78
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellColorFore method, ITextRow.SetCellColorFore, ITextRow::SetCellColorFore, SetCellColorFore, SetCellColorFore method [Windows Controls], SetCellColorFore method [Windows Controls],ITextRow interface, controls.itextrow_setcellcolorfore, tom/ITextRow::SetCellColorFore
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
 - ITextRow::SetCellColorFore
 - tom/ITextRow::SetCellColorFore
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
 - ITextRow.SetCellColorFore
---

# ITextRow::SetCellColorFore


## -description

Sets the foreground color of the active cell.

## -parameters

### -param Value [in]

Type: <b>long</b>

The foreground color.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 See <a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellshading">ITextRow::GetCellShading</a> to see how the foreground color is used together with the background color.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellcolorfore">ITextRow::GetCellColorFore</a>