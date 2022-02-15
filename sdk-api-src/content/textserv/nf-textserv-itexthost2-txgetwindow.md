---
UID: NF:textserv.ITextHost2.TxGetWindow
title: ITextHost2::TxGetWindow (textserv.h)
description: Retrieves the handle of the text host window for the rich edit control.
helpviewer_keywords: ["ITextHost2 interface [Windows Controls]","TxGetWindow method","ITextHost2.TxGetWindow","ITextHost2::TxGetWindow","TxGetWindow","TxGetWindow method [Windows Controls]","TxGetWindow method [Windows Controls]","ITextHost2 interface","controls.itexthost2_txgetwindow","textserv/ITextHost2::TxGetWindow"]
old-location: controls\itexthost2_txgetwindow.htm
tech.root: Controls
ms.assetid: 42594B92-298B-4659-87EC-D10C6996CECF
ms.date: 12/05/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxGetWindow method, ITextHost2.TxGetWindow, ITextHost2::TxGetWindow, TxGetWindow, TxGetWindow method [Windows Controls], TxGetWindow method [Windows Controls],ITextHost2 interface, controls.itexthost2_txgetwindow, textserv/ITextHost2::TxGetWindow
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
 - ITextHost2::TxGetWindow
 - textserv/ITextHost2::TxGetWindow
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
 - ITextHost2.TxGetWindow
---

# ITextHost2::TxGetWindow


## -description

Retrieves the handle of the text host window for the rich edit control.

## -parameters

### -param phwnd

Type: <b>HWND*</b>

The handle of the text host window.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost2">ITextHost2</a>