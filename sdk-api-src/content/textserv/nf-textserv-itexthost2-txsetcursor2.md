---
UID: NF:textserv.ITextHost2.TxSetCursor2
title: ITextHost2::TxSetCursor2 (textserv.h)
description: Sets the shape of the cursor in the text host window.
helpviewer_keywords: ["ITextHost2 interface [Windows Controls]","TxSetCursor2 method","ITextHost2.TxSetCursor2","ITextHost2::TxSetCursor2","TxSetCursor2","TxSetCursor2 method [Windows Controls]","TxSetCursor2 method [Windows Controls]","ITextHost2 interface","controls.itexthost2_txsetcursor2","textserv/ITextHost2::TxSetCursor2"]
old-location: controls\itexthost2_txsetcursor2.htm
tech.root: Controls
ms.assetid: 9671AEEC-CA31-4CE7-8B40-57859E36EF23
ms.date: 12/05/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxSetCursor2 method, ITextHost2.TxSetCursor2, ITextHost2::TxSetCursor2, TxSetCursor2, TxSetCursor2 method [Windows Controls], TxSetCursor2 method [Windows Controls],ITextHost2 interface, controls.itexthost2_txsetcursor2, textserv/ITextHost2::TxSetCursor2
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
 - ITextHost2::TxSetCursor2
 - textserv/ITextHost2::TxSetCursor2
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
 - ITextHost2.TxSetCursor2
---

# ITextHost2::TxSetCursor2


## -description

Sets the shape of the cursor in the text host window.

## -parameters

### -param hcur

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HCURSOR</a></b>

The new cursor shape.

### -param bText

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the cursor is used for text, or <b>FALSE</b> if not.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HCURSOR</a></b>

Returns the cursor that <i>hcur</i> is replacing.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost2">ITextHost2</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txsetcursor">ITextHost::TxSetCursor</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxsetcursor">ITextServices::OnTxSetCursor</a>