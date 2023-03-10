---
UID: NF:textserv.ITextHost.TxGetViewInset
title: ITextHost::TxGetViewInset (textserv.h)
description: Requests the dimensions of the white space inset around the text in the text host window.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxGetViewInset method","ITextHost.TxGetViewInset","ITextHost::TxGetViewInset","TxGetViewInset","TxGetViewInset method [Windows Controls]","TxGetViewInset method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxGetViewInset","_win32_ITextHost_TxGetViewInset_cpp","controls.ITextHost_TxGetViewInset","controls._win32_ITextHost_TxGetViewInset","textserv/ITextHost::TxGetViewInset"]
old-location: controls\ITextHost_TxGetViewInset.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\itexthost\itexthosttxgetviewinset.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxGetViewInset method, ITextHost.TxGetViewInset, ITextHost::TxGetViewInset, TxGetViewInset, TxGetViewInset method [Windows Controls], TxGetViewInset method [Windows Controls],ITextHost interface, _win32_ITextHost_TxGetViewInset, _win32_ITextHost_TxGetViewInset_cpp, controls.ITextHost_TxGetViewInset, controls._win32_ITextHost_TxGetViewInset, textserv/ITextHost::TxGetViewInset
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
 - ITextHost::TxGetViewInset
 - textserv/ITextHost::TxGetViewInset
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
 - ITextHost.TxGetViewInset
---

# ITextHost::TxGetViewInset


## -description

Requests the dimensions of the white space inset around the text in the text host window.

## -parameters

### -param prc

Type: <b>LPRECT</b>

The inset size, in client coordinates. The top, bottom, left, and right members of the 
					<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure indicate how far in each direction the drawing should be inset.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The return value is <b>S_OK</b>.

## -remarks

The view inset is the amount of space on each side between the client rectangle and the view rectangle. The view rectangle (also called the Formatting rectangle) is the rectangle in which the text should be formatted .

The view insets are passed in a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure, but this is not really a rectangle. It should be treated as four independent values to subtract on each side of the client rectangle to figure the view rectangle.

The view insets are passed in HIMETRIC (each HIMETRIC unit corresponds to 0.01 millimeter) so that they do not depend on the client rectangle and the rendering device context.

View insets can be negative on either side of the client rectangle, leading to a bigger view rectangle than the client rectangle. The text should then be clipped to the client rectangle. If the view rectangle is wider than the client rectangle, then the host may add a horizontal scroll bar to the control.

Single line–text services objects ignore the right boundary of the view rectangle when formatting text.

The view inset is available from the host at all times, active or inactive.

## -see-also

<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls Overview</a>