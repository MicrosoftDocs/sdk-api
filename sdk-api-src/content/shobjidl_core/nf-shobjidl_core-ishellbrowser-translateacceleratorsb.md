---
UID: NF:shobjidl_core.IShellBrowser.TranslateAcceleratorSB
title: IShellBrowser::TranslateAcceleratorSB (shobjidl_core.h)
description: Translates accelerator keystrokes intended for the browser's frame while the view is active.
helpviewer_keywords: ["IShellBrowser interface [Windows Shell]","TranslateAcceleratorSB method","IShellBrowser.TranslateAcceleratorSB","IShellBrowser::TranslateAcceleratorSB","TranslateAcceleratorSB","TranslateAcceleratorSB method [Windows Shell]","TranslateAcceleratorSB method [Windows Shell]","IShellBrowser interface","_win32_IShellBrowser_TranslateAcceleratorSB","shell.IShellBrowser_TranslateAcceleratorSB","shobjidl_core/IShellBrowser::TranslateAcceleratorSB"]
old-location: shell\IShellBrowser_TranslateAcceleratorSB.htm
tech.root: shell
ms.assetid: dda5c085-7199-4b83-b03e-e4c715665157
ms.date: 12/05/2018
ms.keywords: IShellBrowser interface [Windows Shell],TranslateAcceleratorSB method, IShellBrowser.TranslateAcceleratorSB, IShellBrowser::TranslateAcceleratorSB, TranslateAcceleratorSB, TranslateAcceleratorSB method [Windows Shell], TranslateAcceleratorSB method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_TranslateAcceleratorSB, shell.IShellBrowser_TranslateAcceleratorSB, shobjidl_core/IShellBrowser::TranslateAcceleratorSB
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
 - IShellBrowser::TranslateAcceleratorSB
 - shobjidl_core/IShellBrowser::TranslateAcceleratorSB
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
 - IShellBrowser.TranslateAcceleratorSB
---

# IShellBrowser::TranslateAcceleratorSB


## -description

Translates accelerator keystrokes intended for the browser's frame while the view is active.

## -parameters

### -param pmsg

Type: <b>LPMSG</b>

The address of an <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure containing the keystroke message.

### -param wID

Type: <b>WORD</b>

The command identifier value corresponding to the keystroke in the container-provided accelerator table. Containers should use this value instead of translating again.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or a COM-defined error value otherwise.

## -remarks

This method is similar to the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-translateaccelerator">IOleInPlaceFrame::TranslateAccelerator</a> method.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>