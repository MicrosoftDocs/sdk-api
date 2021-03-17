---
UID: NF:vfw.MCIWndSetZoom
title: MCIWndSetZoom macro (vfw.h)
description: The MCIWndSetZoom macro resizes a video image according to a zoom factor. This marco adjusts the size of an MCIWnd window while maintaining a constant aspect ratio. You can use this macro or explicitly send the MCIWNDM_SETZOOM message.
helpviewer_keywords: ["MCIWndSetZoom","MCIWndSetZoom macro [Windows Multimedia]","_win32_MCIWndSetZoom","multimedia.mciwndsetzoom","vfw/MCIWndSetZoom"]
old-location: multimedia\mciwndsetzoom.htm
tech.root: Multimedia
ms.assetid: a9912c5c-2336-48a3-aca0-d0d434b9db08
ms.date: 12/05/2018
ms.keywords: MCIWndSetZoom, MCIWndSetZoom macro [Windows Multimedia], _win32_MCIWndSetZoom, multimedia.mciwndsetzoom, vfw/MCIWndSetZoom
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
 - MCIWndSetZoom
 - vfw/MCIWndSetZoom
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
 - MCIWndSetZoom
---

# MCIWndSetZoom macro


## -description

The <b>MCIWndSetZoom</b> macro resizes a video image according to a zoom factor. This marco adjusts the size of an MCIWnd window while maintaining a constant aspect ratio. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-setzoom">MCIWNDM_SETZOOM</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param iZoom

Zoom factor expressed as a percentage of the original image. Specify 100 to display the image at its authored size, 200 to display the image at twice its normal size, or 50 to display the image at half its normal size.