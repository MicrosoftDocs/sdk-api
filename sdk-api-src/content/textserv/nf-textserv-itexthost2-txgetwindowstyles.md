---
UID: NF:textserv.ITextHost2.TxGetWindowStyles
title: ITextHost2::TxGetWindowStyles (textserv.h)
description: Retrieves the window styles and extended windows styles of the text host window.
helpviewer_keywords: ["ITextHost2 interface [Windows Controls]","TxGetWindowStyles method","ITextHost2.TxGetWindowStyles","ITextHost2::TxGetWindowStyles","TxGetWindowStyles","TxGetWindowStyles method [Windows Controls]","TxGetWindowStyles method [Windows Controls]","ITextHost2 interface","controls.itexthost2_txgetwindowstyles","textserv/ITextHost2::TxGetWindowStyles"]
old-location: controls\itexthost2_txgetwindowstyles.htm
tech.root: Controls
ms.assetid: 51885B3E-3DEE-461C-8625-3DE9D8C1F992
ms.date: 12/05/2018
ms.keywords: ITextHost2 interface [Windows Controls],TxGetWindowStyles method, ITextHost2.TxGetWindowStyles, ITextHost2::TxGetWindowStyles, TxGetWindowStyles, TxGetWindowStyles method [Windows Controls], TxGetWindowStyles method [Windows Controls],ITextHost2 interface, controls.itexthost2_txgetwindowstyles, textserv/ITextHost2::TxGetWindowStyles
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
 - ITextHost2::TxGetWindowStyles
 - textserv/ITextHost2::TxGetWindowStyles
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
 - ITextHost2.TxGetWindowStyles
---

# ITextHost2::TxGetWindowStyles


## -description

Retrieves the window styles and extended windows styles of the text host window.

## -parameters

### -param pdwStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

The window styles. For a description of the possible values, see <a href="/windows/desktop/winmsg/window-styles">Window Styles</a>.

### -param pdwExStyle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

The extended windows styles. For a description of the possible values, see <a href="/windows/desktop/winmsg/extended-window-styles">Extended Window Styles</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost2">ITextHost2</a>