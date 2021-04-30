---
UID: NF:vfw.MCIWndSetTimers
title: MCIWndSetTimers macro (vfw.h)
description: The MCIWndSetTimers macro sets the update periods used by MCIWnd to update the trackbar in the MCIWnd window, update the position information displayed in the window title bar, and send notification messages to the parent window.
helpviewer_keywords: ["MCIWndSetTimers","MCIWndSetTimers macro [Windows Multimedia]","_win32_MCIWndSetTimers","multimedia.mciwndsettimers","vfw/MCIWndSetTimers"]
old-location: multimedia\mciwndsettimers.htm
tech.root: Multimedia
ms.assetid: 0a1b1c87-714b-438f-b865-5f5798cb4cf3
ms.date: 12/05/2018
ms.keywords: MCIWndSetTimers, MCIWndSetTimers macro [Windows Multimedia], _win32_MCIWndSetTimers, multimedia.mciwndsettimers, vfw/MCIWndSetTimers
req.header: vfw.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MCIWndSetTimers
 - vfw/MCIWndSetTimers
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndSetTimers
---

# MCIWndSetTimers macro


## -description

The <b>MCIWndSetTimers</b> macro sets the update periods used by MCIWnd to update the trackbar in the MCIWnd window, update the position information displayed in the window title bar, and send notification messages to the parent window. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-settimers">MCIWNDM_SETTIMERS</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param active

Update period used by MCIWnd when it is the active window. The default value is 500 milliseconds. Storage for this value is limited to 16 bits.

### -param inactive

Update period used by MCIWnd when it is the inactive window. The default value is 2000 milliseconds. Storage for this value is limited to 16 bits.