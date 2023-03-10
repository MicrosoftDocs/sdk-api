---
UID: NF:shobjidl_core.IShellLinkW.GetHotkey
title: IShellLinkW::GetHotkey (shobjidl_core.h)
description: Gets the keyboard shortcut (hot key) for a Shell link object. (Unicode)
helpviewer_keywords: ["GetHotkey","GetHotkey method [Windows Shell]","GetHotkey method [Windows Shell]","IShellLink interface","GetHotkey method [Windows Shell]","IShellLinkA interface","GetHotkey method [Windows Shell]","IShellLinkW interface","HOTKEYF_ALT","HOTKEYF_CONTROL","HOTKEYF_EXT","HOTKEYF_SHIFT","IShellLink interface [Windows Shell]","GetHotkey method","IShellLink::GetHotkey","IShellLinkA interface [Windows Shell]","GetHotkey method","IShellLinkA::GetHotkey","IShellLinkW interface [Windows Shell]","GetHotkey method","IShellLinkW.GetHotkey","IShellLinkW::GetHotkey","_win32_IShellLink_GetHotkey","shell.IShellLink_GetHotkey","shobjidl_core/IShellLink::GetHotkey","shobjidl_core/IShellLinkA::GetHotkey","shobjidl_core/IShellLinkW::GetHotkey"]
old-location: shell\IShellLink_GetHotkey.htm
tech.root: shell
ms.assetid: 4e3572bf-8d68-4485-99e8-bf47192be821
ms.date: 12/05/2018
ms.keywords: GetHotkey, GetHotkey method [Windows Shell], GetHotkey method [Windows Shell],IShellLink interface, GetHotkey method [Windows Shell],IShellLinkA interface, GetHotkey method [Windows Shell],IShellLinkW interface, HOTKEYF_ALT, HOTKEYF_CONTROL, HOTKEYF_EXT, HOTKEYF_SHIFT, IShellLink interface [Windows Shell],GetHotkey method, IShellLink::GetHotkey, IShellLinkA interface [Windows Shell],GetHotkey method, IShellLinkA::GetHotkey, IShellLinkW interface [Windows Shell],GetHotkey method, IShellLinkW.GetHotkey, IShellLinkW::GetHotkey, _win32_IShellLink_GetHotkey, shell.IShellLink_GetHotkey, shobjidl_core/IShellLink::GetHotkey, shobjidl_core/IShellLinkA::GetHotkey, shobjidl_core/IShellLinkW::GetHotkey
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
 - IShellLinkW::GetHotkey
 - shobjidl_core/IShellLinkW::GetHotkey
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
 - IShellLink.GetHotkey
 - IShellLinkA.GetHotkey
 - IShellLinkW.GetHotkey
---

# IShellLinkW::GetHotkey


## -description

Gets the keyboard shortcut (hot key) for a Shell link object.

## -parameters

### -param pwHotkey

Type: <b>WORD*</b>

The address of the keyboard shortcut. The virtual key code is in the low-order byte, and the modifier flags are in the high-order byte. The modifier flags can be a combination of the following values.



#### HOTKEYF_ALT

ALT key



#### HOTKEYF_CONTROL

CTRL key



#### HOTKEYF_EXT

Extended key



#### HOTKEYF_SHIFT

SHIFT key


##### - pwHotkey.HOTKEYF_ALT

ALT key


##### - pwHotkey.HOTKEYF_CONTROL

CTRL key


##### - pwHotkey.HOTKEYF_EXT

Extended key


##### - pwHotkey.HOTKEYF_SHIFT

SHIFT key

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

