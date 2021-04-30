---
UID: NF:vfw.MCIWndSetRepeat
title: MCIWndSetRepeat macro (vfw.h)
description: The MCIWndSetRepeat macro sets the repeat flag associated with continuous playback. You can use this macro or explicitly send the MCIWNDM_SETREPEAT message.
helpviewer_keywords: ["MCIWndSetRepeat","MCIWndSetRepeat macro [Windows Multimedia]","_win32_MCIWndSetRepeat","multimedia.mciwndsetrepeat","vfw/MCIWndSetRepeat"]
old-location: multimedia\mciwndsetrepeat.htm
tech.root: Multimedia
ms.assetid: e9c64f01-dd51-4f45-bf58-e930d5d23461
ms.date: 12/05/2018
ms.keywords: MCIWndSetRepeat, MCIWndSetRepeat macro [Windows Multimedia], _win32_MCIWndSetRepeat, multimedia.mciwndsetrepeat, vfw/MCIWndSetRepeat
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
 - MCIWndSetRepeat
 - vfw/MCIWndSetRepeat
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
 - MCIWndSetRepeat
---

# MCIWndSetRepeat macro


## -description

The <b>MCIWndSetRepeat</b> macro sets the repeat flag associated with continuous playback. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-setrepeat">MCIWNDM_SETREPEAT</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

### -param f

New state of the repeat flag. Specify <b>TRUE</b> to turn on continuous playback.

## -remarks

The <b>MCIWndSetRepeat</b> macro only affects playback that the user initiates by hitting the play button on the toolbar. It will not affect playback started with the <b>MCIWndPlay</b> macro.

Currently, MCIAVI is the only device that supports continuous playback.