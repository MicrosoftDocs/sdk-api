---
UID: NF:tom.ITextRow.GetHeight
title: ITextRow::GetHeight (tom.h)
description: Gets the height of the row.
helpviewer_keywords: ["GetHeight","GetHeight method [Windows Controls]","GetHeight method [Windows Controls]","ITextRow interface","ITextRow interface [Windows Controls]","GetHeight method","ITextRow.GetHeight","ITextRow::GetHeight","controls.itextrow_getheight","tom/ITextRow::GetHeight"]
old-location: controls\itextrow_getheight.htm
tech.root: Controls
ms.assetid: 6befda1a-1a47-4668-b0cf-4fd66e7b633d
ms.date: 12/05/2018
ms.keywords: GetHeight, GetHeight method [Windows Controls], GetHeight method [Windows Controls],ITextRow interface, ITextRow interface [Windows Controls],GetHeight method, ITextRow.GetHeight, ITextRow::GetHeight, controls.itextrow_getheight, tom/ITextRow::GetHeight
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
 - ITextRow::GetHeight
 - tom/ITextRow::GetHeight
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
 - ITextRow.GetHeight
---

# ITextRow::GetHeight


## -description

Gets the height of the row.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The row height. A value of 0 indicates autoheight.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrow">ITextRow</a>



<a href="/windows/desktop/api/tom/nf-tom-itextrow-setheight">ITextRow::SetHeight</a>