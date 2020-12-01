---
UID: NF:shobjidl_core.IShellBrowser.SendControlMsg
title: IShellBrowser::SendControlMsg (shobjidl_core.h)
description: Sends control messages to either the toolbar or the status bar in a Windows Explorer window.
helpviewer_keywords: ["IShellBrowser interface [Windows Shell]","SendControlMsg method","IShellBrowser.SendControlMsg","IShellBrowser::SendControlMsg","SendControlMsg","SendControlMsg method [Windows Shell]","SendControlMsg method [Windows Shell]","IShellBrowser interface","_win32_IShellBrowser_SendControlMsg","shell.IShellBrowser_SendControlMsg","shobjidl_core/IShellBrowser::SendControlMsg"]
old-location: shell\IShellBrowser_SendControlMsg.htm
tech.root: shell
ms.assetid: 4494870b-45a8-478a-807a-7ed3674f69f3
ms.date: 12/05/2018
ms.keywords: IShellBrowser interface [Windows Shell],SendControlMsg method, IShellBrowser.SendControlMsg, IShellBrowser::SendControlMsg, SendControlMsg, SendControlMsg method [Windows Shell], SendControlMsg method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_SendControlMsg, shell.IShellBrowser_SendControlMsg, shobjidl_core/IShellBrowser::SendControlMsg
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellBrowser::SendControlMsg
 - shobjidl_core/IShellBrowser::SendControlMsg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellBrowser.SendControlMsg
---

# IShellBrowser::SendControlMsg


## -description

Sends control messages to either the toolbar or the status bar in a Windows Explorer window.

## -parameters

### -param id

Type: <b>UINT</b>

An identifier for either a toolbar (<b>FCW_TOOLBAR</b>) or for a status bar window (<b>FCW_STATUS</b>).

### -param uMsg

Type: <b>UINT</b>

The message to be sent to the control.

### -param wParam

Type: <b>WPARAM</b>

The value depends on the message specified in the <i>uMsg</i> parameter.

### -param lParam

Type: <b>LPARAM</b>

The value depends on the message specified in the <i>uMsg</i> parameter.

### -param pret

Type: <b>LRESULT*</b>

The address of the return value of the 
					<a href="/windows/desktop/api/winuser/nf-winuser-sendmessage">SendMessage</a> function.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or a COM-defined error value otherwise.

## -remarks

Refer to the <a href="/windows/desktop/Controls/common-controls-intro">Common Controls</a> documentation for more information on the messages that can be sent to the toolbar or status bar control.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
Use of this call requires diligent attention, because leaving either the status bar or toolbar in an inappropriate state will affect the performance of Windows Explorer.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If your Windows Explorer does not have these controls, you can return <b>E_NOTIMPL</b>.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>