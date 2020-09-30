---
UID: NF:tom.ITextRange2.GetRow
title: ITextRange2::GetRow (tom.h)
description: Gets the row properties in the currently selected row.
helpviewer_keywords: ["GetRow","GetRow method [Windows Controls]","GetRow method [Windows Controls]","ITextRange2 interface","ITextRange2 interface [Windows Controls]","GetRow method","ITextRange2.GetRow","ITextRange2::GetRow","controls.itextrange2_getrow","tom/ITextRange2::GetRow"]
old-location: controls\itextrange2_getrow.htm
tech.root: Controls
ms.assetid: 3f15605a-8f81-4fc4-ad12-5300ecd03c16
ms.date: 12/05/2018
ms.keywords: GetRow, GetRow method [Windows Controls], GetRow method [Windows Controls],ITextRange2 interface, ITextRange2 interface [Windows Controls],GetRow method, ITextRange2.GetRow, ITextRange2::GetRow, controls.itextrange2_getrow, tom/ITextRange2::GetRow
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
 - ITextRange2::GetRow
 - tom/ITextRange2::GetRow
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
 - ITextRange2.GetRow
---

# ITextRange2::GetRow


## -description

Gets the row properties in the currently selected row.

## -parameters

### -param ppRow [out, retval]

Type: <b>ITextRow**</b>

The row properties.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextrange2">ITextRange2</a>