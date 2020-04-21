---
UID: NF:vfw.MCIWndPlayReverse
title: MCIWndPlayReverse macro (vfw.h)
description: The MCIWndPlayReverse macro plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback.helpviewer_keywords: ["MCIWndPlayReverse","MCIWndPlayReverse macro [Windows Multimedia]","_win32_MCIWndPlayReverse","multimedia.mciwndplayreverse","vfw/MCIWndPlayReverse"]
old-location: multimedia\mciwndplayreverse.htm
tech.root: Multimedia
ms.assetid: 1f3c9c98-a8f5-4ad9-bef9-5d685076df9d
ms.date: 12/05/2018
ms.keywords: MCIWndPlayReverse, MCIWndPlayReverse macro [Windows Multimedia], _win32_MCIWndPlayReverse, multimedia.mciwndplayreverse, vfw/MCIWndPlayReverse
f1_keywords:
- vfw/MCIWndPlayReverse
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vfw.h
api_name:
- MCIWndPlayReverse
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MCIWndPlayReverse macro


## -description



The <b>MCIWndPlayReverse</b> macro plays the current content in the reverse direction, beginning at the current position and ending at the beginning of the content or until another command stops playback. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mciwndm-playreverse">MCIWNDM_PLAYREVERSE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 

