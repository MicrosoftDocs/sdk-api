---
UID: NF:imm.ImmGetDefaultIMEWnd
title: ImmGetDefaultIMEWnd function (imm.h)
description: The ImmGetDefaultIMEWnd function (imm.h) retrieves the default window handle to the IME class.
helpviewer_keywords: ["ImmGetDefaultIMEWnd","ImmGetDefaultIMEWnd function [Internationalization for Windows Applications]","_win32_ImmGetDefaultIMEWnd","imm/ImmGetDefaultIMEWnd","intl.immgetdefaultimewnd"]
old-location: intl\immgetdefaultimewnd.htm
tech.root: Intl
ms.assetid: fc3cdfc2-fcdc-4682-b391-83ea4bb1571f
ms.date: 08/04/2022
ms.keywords: ImmGetDefaultIMEWnd, ImmGetDefaultIMEWnd function [Internationalization for Windows Applications], _win32_ImmGetDefaultIMEWnd, imm/ImmGetDefaultIMEWnd, intl.immgetdefaultimewnd
req.header: imm.h
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
 - ImmGetDefaultIMEWnd
 - imm/ImmGetDefaultIMEWnd
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
 - ImmGetDefaultIMEWnd
---

# ImmGetDefaultIMEWnd function


## -description

Retrieves the default window handle to the IME class.

## -parameters

### -param HWND [in]

Handle to the window.

## -returns

Returns the default window handle to the IME class if successful, or <b>NULL</b> otherwise.

## -remarks

The operating system creates a default IME window for every thread. The window is created based on the IME class. The application can send the <a href="/windows/desktop/Intl/wm-ime-control">WM_IME_CONTROL</a> message to this window.

## -see-also

<a href="/windows/desktop/Intl/input-method-manager">Input Method Manager</a>



<a href="/windows/desktop/Intl/input-method-manager-functions">Input Method Manager Functions</a>



<a href="/windows/desktop/Intl/wm-ime-control">WM_IME_CONTROL</a>
