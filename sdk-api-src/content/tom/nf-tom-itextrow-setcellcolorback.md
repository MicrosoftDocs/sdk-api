---
UID: NF:tom.ITextRow.SetCellColorBack
title: ITextRow::SetCellColorBack (tom.h)
description: Sets the background color of the active cell.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetCellColorBack method","ITextRow.SetCellColorBack","ITextRow::SetCellColorBack","SetCellColorBack","SetCellColorBack method [Windows Controls]","SetCellColorBack method [Windows Controls]","ITextRow interface","controls.itextrow_setcellcolorback","tom/ITextRow::SetCellColorBack"]
old-location: controls\itextrow_setcellcolorback.htm
tech.root: Controls
ms.assetid: 3e0a7bb6-e146-4e51-abc0-e89f9faed235
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetCellColorBack method, ITextRow.SetCellColorBack, ITextRow::SetCellColorBack, SetCellColorBack, SetCellColorBack method [Windows Controls], SetCellColorBack method [Windows Controls],ITextRow interface, controls.itextrow_setcellcolorback, tom/ITextRow::SetCellColorBack
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
 - ITextRow::SetCellColorBack
 - tom/ITextRow::SetCellColorBack
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
 - ITextRow.SetCellColorBack
---

# ITextRow::SetCellColorBack


## -description

Sets the background color of the active cell.

## -parameters

### -param Value [in]

Type: <b>long</b>

The background color.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 See <a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellshading">ITextRow::GetCellShading</a> to see how the background color is used together with the foreground color.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getcellcolorback">ITextRow::GetCellColorBack</a>