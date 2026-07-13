---
UID: NF:immdev.ImmGetVirtualKey
title: ImmGetVirtualKey function (immdev.h)
description: The ImmGetVirtualKey function (immdev.h) retrieves the original virtual key value associated with a key input message that the IME has already processed.
helpviewer_keywords: ["ImmGetVirtualKey","ImmGetVirtualKey function [Internationalization for Windows Applications]","_win32_ImmGetVirtualKey","imm/ImmGetVirtualKey","intl.immgetvirtualkey"]
old-location: intl\immgetvirtualkey.htm
tech.root: Intl
ms.assetid: 56c40e55-19e3-4c06-bac7-c4d0098e932a
ms.date: 08/04/2022
ms.keywords: ImmGetVirtualKey, ImmGetVirtualKey function [Internationalization for Windows Applications], _win32_ImmGetVirtualKey, imm/ImmGetVirtualKey, intl.immgetvirtualkey
req.header: immdev.h
req.include-header: Immdev.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],East Asian language support installed.
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
req.lib: Imm32.lib
req.dll: Imm32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ImmGetVirtualKey
 - immdev/ImmGetVirtualKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-imm-l1-1-2.dll
 - Imm32.dll
 - Ext-MS-Win-imm-l1-1-0.dll
 - ext-ms-win-imm-l1-1-1.dll
api_name:
 - ImmGetVirtualKey
---

# ImmGetVirtualKey function


## -description

Retrieves the original virtual key value associated with a key input message that the IME has already processed.

## -parameters

### -param HWND [in]

Handle to the window that receives the key message.

## -returns

If <a href="/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a> has been called by the application, <b>ImmGetVirtualKey</b> returns VK_PROCESSKEY; otherwise, it returns the virtual key.

## -remarks

Although the IME sets the virtual key value to VK_PROCESSKEY after processing a key input message, an application can recover the original virtual key value with the <b>ImmGetVirtualKey</b> function. This function is used only for key input messages containing the VK_PROCESSKEY value. Applications can only get the original virtual key by using this function after receiving 

the <a href="/windows/desktop/inputdev/wm-keydown">WM_KEYDOWN</a> (VK_PROCESSKEY) message, and before <a href="/windows/desktop/api/winuser/nf-winuser-translatemessage">TranslateMessage</a> is called in its own 

message loop.

## -see-also

- <a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>
- <a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>
- <a href="/windows/desktop/inputdev/keyboard-input">Keyboard Input</a>
