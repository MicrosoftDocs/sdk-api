---
UID: NF:vfw.MCIWndValidateMedia
title: MCIWndValidateMedia macro (vfw.h)
description: The MCIWndValidateMedia macro updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format.
helpviewer_keywords: ["MCIWndValidateMedia","MCIWndValidateMedia macro [Windows Multimedia]","_win32_MCIWndValidateMedia","multimedia.mciwndvalidatemedia","vfw/MCIWndValidateMedia"]
old-location: multimedia\mciwndvalidatemedia.htm
tech.root: Multimedia
ms.assetid: 25dc3d0c-6718-4155-9a60-e140da0473e8
ms.date: 12/05/2018
ms.keywords: MCIWndValidateMedia, MCIWndValidateMedia macro [Windows Multimedia], _win32_MCIWndValidateMedia, multimedia.mciwndvalidatemedia, vfw/MCIWndValidateMedia
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
 - MCIWndValidateMedia
 - vfw/MCIWndValidateMedia
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
 - MCIWndValidateMedia
---

# MCIWndValidateMedia macro


## -description

The <b>MCIWndValidateMedia</b> macro updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format. You can use this macro or explicitly send the <a href="/windows/desktop/Multimedia/mciwndm-validatemedia">MCIWNDM_VALIDATEMEDIA</a> message.

## -parameters

### -param hwnd

Handle of the MCIWnd window.

## -remarks

Typically, you should not need to use this macro; however, if your application changes the time format of a device without using MCIWnd; the starting and ending locations of the content, as well as the trackbar, continue to use the old format. You can use this macro to update these values.