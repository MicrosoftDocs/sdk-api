---
UID: NF:shobjidl_core.IShellLinkW.SetHotkey
title: IShellLinkW::SetHotkey (shobjidl_core.h)
description: Sets a keyboard shortcut (hot key) for a Shell link object. (Unicode)
helpviewer_keywords: ["IShellLink interface [Windows Shell]","SetHotkey method","IShellLink::SetHotkey","IShellLinkA interface [Windows Shell]","SetHotkey method","IShellLinkA::SetHotkey","IShellLinkW interface [Windows Shell]","SetHotkey method","IShellLinkW.SetHotkey","IShellLinkW::SetHotkey","SetHotkey","SetHotkey method [Windows Shell]","SetHotkey method [Windows Shell]","IShellLink interface","SetHotkey method [Windows Shell]","IShellLinkA interface","SetHotkey method [Windows Shell]","IShellLinkW interface","_win32_IShellLink_SetHotkey","shell.IShellLink_SetHotkey","shobjidl_core/IShellLink::SetHotkey","shobjidl_core/IShellLinkA::SetHotkey","shobjidl_core/IShellLinkW::SetHotkey"]
old-location: shell\IShellLink_SetHotkey.htm
tech.root: shell
ms.assetid: 82cc2af8-b872-4efc-bfe4-04a50df74e28
ms.date: 12/05/2018
ms.keywords: IShellLink interface [Windows Shell],SetHotkey method, IShellLink::SetHotkey, IShellLinkA interface [Windows Shell],SetHotkey method, IShellLinkA::SetHotkey, IShellLinkW interface [Windows Shell],SetHotkey method, IShellLinkW.SetHotkey, IShellLinkW::SetHotkey, SetHotkey, SetHotkey method [Windows Shell], SetHotkey method [Windows Shell],IShellLink interface, SetHotkey method [Windows Shell],IShellLinkA interface, SetHotkey method [Windows Shell],IShellLinkW interface, _win32_IShellLink_SetHotkey, shell.IShellLink_SetHotkey, shobjidl_core/IShellLink::SetHotkey, shobjidl_core/IShellLinkA::SetHotkey, shobjidl_core/IShellLinkW::SetHotkey
req.header: shobjidl_core.h
req.include-header: 
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
 - IShellLinkW::SetHotkey
 - shobjidl_core/IShellLinkW::SetHotkey
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
 - IShellLink.SetHotkey
 - IShellLinkA.SetHotkey
 - IShellLinkW.SetHotkey
---

# IShellLinkW::SetHotkey


## -description

Sets a keyboard shortcut (hot key) for a Shell link object.

## -parameters

### -param wHotkey

Type: <b>WORD</b>

The new keyboard shortcut. The virtual key code is in the low-order byte, and the modifier flags are in the high-order byte. The modifier flags can be a combination of the values specified in the description of the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-gethotkey">IShellLink::GetHotkey</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Setting a keyboard shortcut allows the user to activate the object by pressing a particular combination of keys.
