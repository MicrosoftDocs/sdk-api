---
UID: NF:vfw.MCIWndSetInactiveTimer
title: MCIWndSetInactiveTimer macro (vfw.h)
description: The MCIWndSetInactiveTimer macro sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive. You can use this macro or explicitly send the MCIWNDM_SETINACTIVETIMER message.
helpviewer_keywords: ["MCIWndSetInactiveTimer","MCIWndSetInactiveTimer macro [Windows Multimedia]","_win32_MCIWndSetInactiveTimer","multimedia.mciwndsetinactivetimer","vfw/MCIWndSetInactiveTimer"]
old-location: multimedia\mciwndsetinactivetimer.htm
tech.root: Multimedia
ms.assetid: 2a0d45dc-1df6-4b1a-b4bc-3704257c5b38
ms.date: 12/05/2018
ms.keywords: MCIWndSetInactiveTimer, MCIWndSetInactiveTimer macro [Windows Multimedia], _win32_MCIWndSetInactiveTimer, multimedia.mciwndsetinactivetimer, vfw/MCIWndSetInactiveTimer
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
 - MCIWndSetInactiveTimer
 - vfw/MCIWndSetInactiveTimer
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
 - MCIWndSetInactiveTimer
---

# MCIWndSetInactiveTimer macro


## -description

The <b>MCIWndSetInactiveTimer</b> macro sets the update period used by MCIWnd to update the trackbar in the MCIWnd window, update position information displayed in the window title bar, and send notification messages to the parent window when the MCIWnd window is inactive. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-setinactivetimer">MCIWNDM_SETINACTIVETIMER</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param inactive

Update period, in milliseconds. The default is 2000 milliseconds.