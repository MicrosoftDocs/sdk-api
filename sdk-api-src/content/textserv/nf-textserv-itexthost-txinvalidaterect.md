---
UID: NF:textserv.ITextHost.TxInvalidateRect
title: ITextHost::TxInvalidateRect (textserv.h)
description: Specifies a rectangle for the text host to add to the update region of the text host window.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxInvalidateRect method","ITextHost.TxInvalidateRect","ITextHost::TxInvalidateRect","TxInvalidateRect","TxInvalidateRect method [Windows Controls]","TxInvalidateRect method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxInvalidateRect","_win32_ITextHost_TxInvalidateRect_cpp","controls.ITextHost_TxInvalidateRect","controls._win32_ITextHost_TxInvalidateRect","textserv/ITextHost::TxInvalidateRect"]
old-location: controls\ITextHost_TxInvalidateRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxinvalidaterect.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxInvalidateRect method, ITextHost.TxInvalidateRect, ITextHost::TxInvalidateRect, TxInvalidateRect, TxInvalidateRect method [Windows Controls], TxInvalidateRect method [Windows Controls],ITextHost interface, _win32_ITextHost_TxInvalidateRect, _win32_ITextHost_TxInvalidateRect_cpp, controls.ITextHost_TxInvalidateRect, controls._win32_ITextHost_TxInvalidateRect, textserv/ITextHost::TxInvalidateRect
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
 - ITextHost::TxInvalidateRect
 - textserv/ITextHost::TxInvalidateRect
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
 - ITextHost.TxInvalidateRect
---

# ITextHost::TxInvalidateRect


## -description

Specifies a rectangle for the text host to add to the update region of the text host window.

## -parameters

### -param prc [in]

Type: <b>LPCRECT</b>

The invalid rectangle.

### -param fMode [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Specifies whether the background within the update region is to be erased when the update region is processed. If this parameter is <b>TRUE</b>, the background is erased when the <a href="/windows/desktop/api/winuser/nf-winuser-beginpaint">BeginPaint</a> function is called. If this parameter is <b>FALSE</b>, the background remains unchanged.

## -remarks

This function may be called while inactive; however, the host implementation is free to invalidate an area greater than the requested 
				<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>