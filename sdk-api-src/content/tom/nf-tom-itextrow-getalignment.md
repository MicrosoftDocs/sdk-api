---
UID: NF:tom.ITextRow.GetAlignment
title: ITextRow::GetAlignment (tom.h)
description: Gets the horizontal alignment of a row.
helpviewer_keywords: ["GetAlignment","GetAlignment method [Windows Controls]","GetAlignment method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetAlignment method","ITextRow.GetAlignment","ITextRow::GetAlignment","controls.itextrow_getalignment","tom/ITextRow::GetAlignment"]
old-location: controls\itextrow_getalignment.htm
tech.root: Controls
ms.assetid: 2c7279b0-6329-4abd-a719-da4ed4d71c71
ms.date: 12/05/2018
ms.keywords: GetAlignment, GetAlignment method [Windows Controls], GetAlignment method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetAlignment method, ITextRow.GetAlignment, ITextRow::GetAlignment, controls.itextrow_getalignment, tom/ITextRow::GetAlignment
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
 - ITextRow::GetAlignment
 - tom/ITextRow::GetAlignment
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
 - ITextRow.GetAlignment
---

# ITextRow::GetAlignment


## -description

Gets the horizontal alignment of a row.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The horizontal alignment. It can be one of the following values.

<p class="indent"><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomAlignLeft</a>

<p class="indent"><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomAlignCenter</a>

<p class="indent"><a href="/windows/win32/api/tom/ne-tom-tomconstants">tomAlignRight</a>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setalignment">ITextRow::SetAlignment</a>