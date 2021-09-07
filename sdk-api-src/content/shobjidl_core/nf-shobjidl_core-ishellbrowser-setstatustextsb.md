---
UID: NF:shobjidl_core.IShellBrowser.SetStatusTextSB
title: IShellBrowser::SetStatusTextSB (shobjidl_core.h)
description: Sets and displays status text about the in-place object in the container's frame-window status bar.
helpviewer_keywords: ["IShellBrowser interface [Windows Shell]","SetStatusTextSB method","IShellBrowser.SetStatusTextSB","IShellBrowser::SetStatusTextSB","SetStatusTextSB","SetStatusTextSB method [Windows Shell]","SetStatusTextSB method [Windows Shell]","IShellBrowser interface","_win32_IShellBrowser_SetStatusTextSB","shell.IShellBrowser_SetStatusTextSB","shobjidl_core/IShellBrowser::SetStatusTextSB"]
old-location: shell\IShellBrowser_SetStatusTextSB.htm
tech.root: shell
ms.assetid: d7dd9f17-41e4-4c04-981e-a0bfe7c53fcf
ms.date: 12/05/2018
ms.keywords: IShellBrowser interface [Windows Shell],SetStatusTextSB method, IShellBrowser.SetStatusTextSB, IShellBrowser::SetStatusTextSB, SetStatusTextSB, SetStatusTextSB method [Windows Shell], SetStatusTextSB method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_SetStatusTextSB, shell.IShellBrowser_SetStatusTextSB, shobjidl_core/IShellBrowser::SetStatusTextSB
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
 - IShellBrowser::SetStatusTextSB
 - shobjidl_core/IShellBrowser::SetStatusTextSB
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
 - IShellBrowser.SetStatusTextSB
---

# IShellBrowser::SetStatusTextSB


## -description

Sets and displays status text about the in-place object in the container's frame-window status bar.

## -parameters

### -param pszStatusText

Type: <b>LPCWSTR</b>

A pointer to a null-terminated character string that contains the message to display.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is also possible to send messages directly to the status window by using the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-sendcontrolmsg">IShellBrowser::SendControlMsg</a> method.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
Use this method to set the contents of the status bar.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>