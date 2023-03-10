---
UID: NF:control.IVideoWindow.NotifyOwnerMessage
title: IVideoWindow::NotifyOwnerMessage (control.h)
description: The NotifyOwnerMessage method forwards a message to the video window.
helpviewer_keywords: ["IVideoWindow interface [DirectShow]","NotifyOwnerMessage method","IVideoWindow.NotifyOwnerMessage","IVideoWindow::NotifyOwnerMessage","IVideoWindowNotifyOwnerMessage","NotifyOwnerMessage","NotifyOwnerMessage method [DirectShow]","NotifyOwnerMessage method [DirectShow]","IVideoWindow interface","control/IVideoWindow::NotifyOwnerMessage","dshow.ivideowindow_notifyownermessage"]
old-location: dshow\ivideowindow_notifyownermessage.htm
tech.root: dshow
ms.assetid: 37d28f32-5da5-4082-ac57-5b274e95ca68
ms.date: 12/05/2018
ms.keywords: IVideoWindow interface [DirectShow],NotifyOwnerMessage method, IVideoWindow.NotifyOwnerMessage, IVideoWindow::NotifyOwnerMessage, IVideoWindowNotifyOwnerMessage, NotifyOwnerMessage, NotifyOwnerMessage method [DirectShow], NotifyOwnerMessage method [DirectShow],IVideoWindow interface, control/IVideoWindow::NotifyOwnerMessage, dshow.ivideowindow_notifyownermessage
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVideoWindow::NotifyOwnerMessage
 - control/IVideoWindow::NotifyOwnerMessage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IVideoWindow.NotifyOwnerMessage
---

# IVideoWindow::NotifyOwnerMessage


## -description

The <code>NotifyOwnerMessage</code> method forwards a message to the video window.

## -parameters

### -param hwnd [in]

A handle to the window, as an <a href="/windows/desktop/DirectShow/oahwnd">OAHWND</a> value.

### -param uMsg [in]

Specifies the message.

### -param wParam [in]

Message parameter.

### -param lParam [in]

Message parameter.

## -returns

Possible return values include the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The video renderer filter is not connected.

</td>
</tr>
</table>

## -remarks

The Filter Graph Manager calls this method to pass various messages to the renderer, including the following:

<ul>
<li>WM_ACTIVATEAPP</li>
<li>WM_DEVMODECHANGE</li>
<li>WM_DISPLAYCHANGE</li>
<li>WM_PALETTECHANGED</li>
<li>WM_PALETTEISCHANGING</li>
<li>WM_QUERYNEWPALETTE</li>
<li>WM_SYSCOLORCHANGE</li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ivideowindow">IVideoWindow Interface</a>