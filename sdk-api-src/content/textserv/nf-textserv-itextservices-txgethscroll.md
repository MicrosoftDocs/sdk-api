---
UID: NF:textserv.ITextServices.TxGetHScroll
title: ITextServices::TxGetHScroll (textserv.h)
description: Returns horizontal scroll bar information.
helpviewer_keywords: ["ITextServices interface [Windows Controls]","TxGetHScroll method","ITextServices.TxGetHScroll","ITextServices::TxGetHScroll","TxGetHScroll","TxGetHScroll method [Windows Controls]","TxGetHScroll method [Windows Controls]","ITextServices interface","_win32_ITextServices_TxGetHScroll","_win32_ITextServices_TxGetHScroll_cpp","controls.ITextServices_TxGetHScroll","controls._win32_ITextServices_TxGetHScroll","textserv/ITextServices::TxGetHScroll"]
old-location: controls\ITextServices_TxGetHScroll.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txgethscroll.htm
ms.date: 12/05/2018
ms.keywords: ITextServices interface [Windows Controls],TxGetHScroll method, ITextServices.TxGetHScroll, ITextServices::TxGetHScroll, TxGetHScroll, TxGetHScroll method [Windows Controls], TxGetHScroll method [Windows Controls],ITextServices interface, _win32_ITextServices_TxGetHScroll, _win32_ITextServices_TxGetHScroll_cpp, controls.ITextServices_TxGetHScroll, controls._win32_ITextServices_TxGetHScroll, textserv/ITextServices::TxGetHScroll
req.header: textserv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ITextServices::TxGetHScroll
 - textserv/ITextServices::TxGetHScroll
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
 - ITextServices.TxGetHScroll
---

# ITextServices::TxGetHScroll


## -description

Returns horizontal scroll bar information.

## -parameters

### -param plMin

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The minimum scroll position.

### -param plMax

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The maximum scroll position.

### -param plPos

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The current scroll position.

### -param plPage

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a>*</b>

The view width, in pixels.

### -param pfEnabled

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Indicates whether horizontal scrolling is enabled. If <b>TRUE</b>, horizontal scrolling is enabled.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The method always returns <b>S_OK</b>.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>