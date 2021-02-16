---
UID: NF:textserv.ITextHost.TxViewChange
title: ITextHost::TxViewChange (textserv.h)
description: Indicates to the text host that the update region has changed.
helpviewer_keywords: ["ITextHost interface [Windows Controls]","TxViewChange method","ITextHost.TxViewChange","ITextHost::TxViewChange","TxViewChange","TxViewChange method [Windows Controls]","TxViewChange method [Windows Controls]","ITextHost interface","_win32_ITextHost_TxViewChange","_win32_ITextHost_TxViewChange_cpp","controls.ITextHost_TxViewChange","controls._win32_ITextHost_TxViewChange","textserv/ITextHost::TxViewChange"]
old-location: controls\ITextHost_TxViewChange.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\richedit\windowlessricheditcontrols\windowlessricheditcontrolsreference\windowlessricheditcontrolinterfaces\txviewchange.htm
ms.date: 12/05/2018
ms.keywords: ITextHost interface [Windows Controls],TxViewChange method, ITextHost.TxViewChange, ITextHost::TxViewChange, TxViewChange, TxViewChange method [Windows Controls], TxViewChange method [Windows Controls],ITextHost interface, _win32_ITextHost_TxViewChange, _win32_ITextHost_TxViewChange_cpp, controls.ITextHost_TxViewChange, controls._win32_ITextHost_TxViewChange, textserv/ITextHost::TxViewChange
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
 - ITextHost::TxViewChange
 - textserv/ITextHost::TxViewChange
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
 - ITextHost.TxViewChange
---

# ITextHost::TxViewChange


## -description

Indicates to the text host that the update region has changed.

## -parameters

### -param fUpdate [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Update flag. If <b>TRUE</b>, the text host calls <a href="/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a>; otherwise it does nothing. See the Remarks section.

## -remarks

The text services object must call <b>TxViewChange</b> every time its visual representation has changed, even if the control is inactive. If the control is active, then text services must also make sure the control's window is updated. It can do this in a number of ways: 

<ul>
<li>Call <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txgetdc">ITextHost::TxGetDC</a> to get a device context for the control's window and then repaint or update the window. Afterward, call <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txreleasedc">ITextHost::TxReleaseDC</a>. </li>
<li>Call <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txinvalidaterect">ITextHost::TxInvalidateRect</a> to invalidate the control's window. </li>
<li>Call <a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txscrollwindowex">ITextHost::TxScrollWindowEx</a> to scroll the control's window. </li>
</ul>
After the text services object has updated the active view, it can call <b>TxViewChange</b> and set <i>fUpdate</i> to <b>TRUE</b> along with the call. By passing <b>TRUE</b>, the text host calls <a href="/windows/desktop/api/winuser/nf-winuser-updatewindow">UpdateWindow</a> to make sure any unpainted areas of the active control are repainted.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/textserv/nl-textserv-itexthost">ITextHost</a>



<b>Reference</b>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txgetdc">TxGetDC</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txinvalidaterect">TxInvalidateRect</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txreleasedc">TxReleaseDC</a>



<a href="/windows/desktop/api/textserv/nf-textserv-itexthost-txscrollwindowex">TxScrollWindowEx</a>



<a href="/windows/desktop/Controls/windowless-rich-edit-controls">Windowless Rich Edit Controls</a>