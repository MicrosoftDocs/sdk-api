---
UID: NF:textserv.ITextHost2.TxGetHorzExtent
title: ITextHost2::TxGetHorzExtent (textserv.h)
description: Gets the horizontal scroll extent of the text host window.
helpviewer_keywords: ["ITextHost2 interface [Windows Controls]","TxGetHorzExtent method","ITextHost2.TxGetHorzExtent","ITextHost2::TxGetHorzExtent","TxGetHorzExtent","TxGetHorzExtent method [Windows Controls]","TxGetHorzExtent method [Windows Controls]","ITextHost2 interface","controls.itexthost2_txgethorzextent","textserv/ITextHost2::TxGetHorzExtent"]
old-location: controls\itexthost2_txgethorzextent.htm
tech.root: Controls
ms.assetid: 86D53FEF-DB50-41F6-AC99-106FC01BCD61
ms.date: 12/05/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxGetHorzExtent method, ITextHost2.TxGetHorzExtent, ITextHost2::TxGetHorzExtent, TxGetHorzExtent, TxGetHorzExtent method [Windows Controls], TxGetHorzExtent method [Windows Controls],ITextHost2 interface, controls.itexthost2_txgethorzextent, textserv/ITextHost2::TxGetHorzExtent
req.header: textserv.h
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
 - ITextHost2::TxGetHorzExtent
 - textserv/ITextHost2::TxGetHorzExtent
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
 - ITextHost2.TxGetHorzExtent
---

# ITextHost2::TxGetHorzExtent


## -description

Gets the horizontal scroll extent of the text host window.

## -parameters

### -param plHorzExtent

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The horizontal scroll extent.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A rich edit control doesn't use the return value; instead, they get the scroll width from the widest line.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost2">ITextHost2</a>