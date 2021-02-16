---
UID: NF:tom.ITextRow.SetAlignment
title: ITextRow::SetAlignment (tom.h)
description: Sets the horizontal alignment of a row.
helpviewer_keywords: ["ITextRow interface [Windows Controls]","SetAlignment method","ITextRow.SetAlignment","ITextRow::SetAlignment","SetAlignment","SetAlignment method [Windows Controls]","SetAlignment method [Windows Controls]","ITextRow interface","controls.itextrow_setalignment","tom/ITextRow::SetAlignment"]
old-location: controls\itextrow_setalignment.htm
tech.root: Controls
ms.assetid: bfcc900d-2bec-4314-a2c5-09f55e27a626
ms.date: 12/05/2018
ms.keywords: ITextRow interface [Windows Controls],SetAlignment method, ITextRow.SetAlignment, ITextRow::SetAlignment, SetAlignment, SetAlignment method [Windows Controls], SetAlignment method [Windows Controls],ITextRow interface, controls.itextrow_setalignment, tom/ITextRow::SetAlignment
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
 - ITextRow::SetAlignment
 - tom/ITextRow::SetAlignment
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
 - ITextRow.SetAlignment
---

# ITextRow::SetAlignment


## -description

Sets the horizontal alignment of a row.

## -parameters

### -param Value [in]

Type: <b>long</b>

The new horizontal alignment. It can be one of the following values.

<p class="indent"><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomAlignLeft</a>

<p class="indent"><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomAlignCenter</a>

<p class="indent"><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomAlignRight</a>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-getalignment">ITextRow::GetAlignment</a>