---
UID: NF:vfw.MCIWndDestroy
title: MCIWndDestroy macro (vfw.h)
description: The MCIWndDestroy macro closes an MCI device or file associated with an MCIWnd window and destroys the window. You can use this macro or explicitly send the WM_CLOSE message.
helpviewer_keywords: ["MCIWndDestroy","MCIWndDestroy macro [Windows Multimedia]","_win32_MCIWndDestroy","multimedia.mciwnddestroy","vfw/MCIWndDestroy"]
old-location: multimedia\mciwnddestroy.htm
tech.root: Multimedia
ms.assetid: 26e11fd1-99fd-4afa-8879-096a40acecce
ms.date: 12/05/2018
ms.keywords: MCIWndDestroy, MCIWndDestroy macro [Windows Multimedia], _win32_MCIWndDestroy, multimedia.mciwnddestroy, vfw/MCIWndDestroy
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
 - MCIWndDestroy
 - vfw/MCIWndDestroy
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
 - MCIWndDestroy
---

# MCIWndDestroy macro


## -description

The <b>MCIWndDestroy</b> macro closes an MCI device or file associated with an MCIWnd window and destroys the window. You can use this macro or explicitly send the <a href="/windows/win32/winmsg/wm-close">WM_CLOSE</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -see-also

<a href="/windows/win32/winmsg/wm-close">WM_CLOSE</a>