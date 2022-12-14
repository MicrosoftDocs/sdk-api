---
UID: NF:textserv.ITextServices.OnTxInPlaceDeactivate
title: ITextServices::OnTxInPlaceDeactivate (textserv.h)
description: Notifies the text services object that this control is no longer in-place active.
helpviewer_keywords: ["ITextServices interface [Windows Controls]","OnTxInPlaceDeactivate method","ITextServices.OnTxInPlaceDeactivate","ITextServices::OnTxInPlaceDeactivate","OnTxInPlaceDeactivate","OnTxInPlaceDeactivate method [Windows Controls]","OnTxInPlaceDeactivate method [Windows Controls]","ITextServices interface","_win32_ITextServices_OnTxInPlaceDeactivate","_win32_ITextServices_OnTxInPlaceDeactivate_cpp","controls.ITextServices_OnTxInPlaceDeactivate","controls._win32_ITextServices_OnTxInPlaceDeactivate","textserv/ITextServices::OnTxInPlaceDeactivate"]
old-location: controls\ITextServices_OnTxInPlaceDeactivate.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\ontxinplacedeactivate.htm
ms.date: 12/05/2018
ms.keywords: ITextServices interface [Windows Controls],OnTxInPlaceDeactivate method, ITextServices.OnTxInPlaceDeactivate, ITextServices::OnTxInPlaceDeactivate, OnTxInPlaceDeactivate, OnTxInPlaceDeactivate method [Windows Controls], OnTxInPlaceDeactivate method [Windows Controls],ITextServices interface, _win32_ITextServices_OnTxInPlaceDeactivate, _win32_ITextServices_OnTxInPlaceDeactivate_cpp, controls.ITextServices_OnTxInPlaceDeactivate, controls._win32_ITextServices_OnTxInPlaceDeactivate, textserv/ITextServices::OnTxInPlaceDeactivate
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
 - ITextServices::OnTxInPlaceDeactivate
 - textserv/ITextServices::OnTxInPlaceDeactivate
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
 - ITextServices.OnTxInPlaceDeactivate
---

# ITextServices::OnTxInPlaceDeactivate


## -description

Notifies the text services object that this control is no longer in-place active.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

The return value is always <b>S_OK</b>.

## -remarks

In-place activation refers to an embedded object <i>running in-place</i> (for example, for regular controls and embeddings, it would have a window to draw in). In contrast, UI active means that an object currently has the <i>editing focus</i>. Specifically, things like menus and toolbars on the container may also contain elements from the UI-active control/embedding. There can only be one UI-active control at any given time, while many can be in-place active at once.

Note, UI activation is different from getting the focus. To let the text services object know that the control is getting or losing focus, the host will send <a href="/windows/desktop/inputdev/wm-setfocus">WM_SETFOCUS</a> and <a href="/windows/desktop/inputdev/wm-killfocus">WM_KILLFOCUS</a> messages. Also, note that a windowless host will pass <b>NULL</b> as the <i>wParam</i> (window that lost the focus) for these messages.

When making the transition from the UI-active state to a nonactive state, the host should call <a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxuideactivate">ITextServices::OnTxUIDeactivate</a> first and then <b>ITextServices::OnTxInPlaceDeactivate</b>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itextservices">ITextServices</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itextservices-ontxuideactivate">OnTxUIDeactivate</a>



<b>Other Resources</b>



<b>Reference</b>



<a href="/windows/desktop/inputdev/wm-killfocus">WM_KILLFOCUS</a>



<a href="/windows/desktop/inputdev/wm-setfocus">WM_SETFOCUS</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>
