---
UID: NF:vfw.MCIWndSetActiveTimer
title: MCIWndSetActiveTimer macro (vfw.h)
description: The MCIWndSetActiveTimer macro sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active. You can use this macro or explicitly send the MCIWNDM_SETACTIVETIMER message.
helpviewer_keywords: ["MCIWndSetActiveTimer","MCIWndSetActiveTimer macro [Windows Multimedia]","_win32_MCIWndSetActiveTimer","multimedia.mciwndsetactivetimer","vfw/MCIWndSetActiveTimer"]
old-location: multimedia\mciwndsetactivetimer.htm
tech.root: Multimedia
ms.assetid: 0a0815c4-6c35-4d67-a87b-d355f9ffbf3b
ms.date: 12/05/2018
ms.keywords: MCIWndSetActiveTimer, MCIWndSetActiveTimer macro [Windows Multimedia], _win32_MCIWndSetActiveTimer, multimedia.mciwndsetactivetimer, vfw/MCIWndSetActiveTimer
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
 - MCIWndSetActiveTimer
 - vfw/MCIWndSetActiveTimer
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
 - MCIWndSetActiveTimer
---

# MCIWndSetActiveTimer macro


## -description

The <b>MCIWndSetActiveTimer</b> macro sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is active. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-setactivetimer">MCIWNDM_SETACTIVETIMER</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param active

Update period, in milliseconds. The default is 500 milliseconds.