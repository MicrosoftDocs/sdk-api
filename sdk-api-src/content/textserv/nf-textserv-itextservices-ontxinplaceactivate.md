---
UID: NF:textserv.ITextServices.OnTxInPlaceActivate
title: ITextServices::OnTxInPlaceActivate (textserv.h)
description: Notifies the text services object that this control is in-place active.
helpviewer_keywords: ["ITextServices interface [Windows Controls]","OnTxInPlaceActivate method","ITextServices.OnTxInPlaceActivate","ITextServices::OnTxInPlaceActivate","OnTxInPlaceActivate","OnTxInPlaceActivate method [Windows Controls]","OnTxInPlaceActivate method [Windows Controls]","ITextServices interface","_win32_ITextServices_OnTxInPlaceActivate","_win32_ITextServices_OnTxInPlaceActivate_cpp","controls.ITextServices_OnTxInPlaceActivate","controls._win32_ITextServices_OnTxInPlaceActivate","textserv/ITextServices::OnTxInPlaceActivate"]
old-location: controls\ITextServices_OnTxInPlaceActivate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxinplaceactivate.htm
ms.date: 12/05/2018
ms.keywords: ITextServices interface [Windows Controls],OnTxInPlaceActivate method, ITextServices.OnTxInPlaceActivate, ITextServices::OnTxInPlaceActivate, OnTxInPlaceActivate, OnTxInPlaceActivate method [Windows Controls], OnTxInPlaceActivate method [Windows Controls],ITextServices interface, _win32_ITextServices_OnTxInPlaceActivate, _win32_ITextServices_OnTxInPlaceActivate_cpp, controls.ITextServices_OnTxInPlaceActivate, controls._win32_ITextServices_OnTxInPlaceActivate, textserv/ITextServices::OnTxInPlaceActivate
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
 - ITextServices::OnTxInPlaceActivate
 - textserv/ITextServices::OnTxInPlaceActivate
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
 - ITextServices.OnTxInPlaceActivate
---

# ITextServices::OnTxInPlaceActivate


## -description

Notifies the text services object that this control is in-place active.

## -parameters

### -param prcClient [in]

Type: <b>const <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>*</b>

The control's client rectangle.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the object is successfully activated, the return value is <b>S_OK</b>.

If the object could not be activated due to error, the return value is E_FAIL. For more information on COM error codes, see <a href="/windows/desktop/com/error-handling-in-com">Error Handling in COM</a>.

## -remarks

In-place active means that an embedded object is <i>running in-place</i> (for example, for regular controls and embeddings, it would have a window to draw in). In contrast, UI active means that an object currently has the <i>editing focus</i>. For example, things like menus and toolbars on the container may also contain elements from the UI-active control/embedding. There is only one UI-active control at any given time, while there can be many in-place active controls.

Note, UI activation is different from getting the focus. To signal the text services object that the control is getting or losing focus, the host sends <a href="/windows/desktop/inputdev/wm-setfocus">WM_SETFOCUS</a> and <a href="/windows/desktop/inputdev/wm-killfocus">WM_KILLFOCUS</a> messages. Also, note that a windowless host will pass <b>NULL</b> as the <i>wParam</i> (window that lost the focus) for these messages.

When making the transition directly from a nonactive state to the UI-active state, the host should call <b>ITextServices::OnTxInPlaceActivate</b> first and then <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxuiactivate">ITextServices::OnTxUIActivate</a>. 

<b>ITextServices::OnTxInPlaceActivate</b> takes as a parameter the client rectangle of the view being activated. This rectangle is given in client coordinates of the containing window. It is the same as would be obtained by calling <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txgetclientrect">TxGetClientRect</a> on the host.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxuiactivate">OnTxUIActivate</a>



<b>Other Resources</b>



<a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a>



<b>Reference</b>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txgetclientrect">TxGetClientRect</a>



<a href="/windows/desktop/inputdev/wm-killfocus">WM_KILLFOCUS</a>



<a href="/windows/desktop/inputdev/wm-setfocus">WM_SETFOCUS</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>