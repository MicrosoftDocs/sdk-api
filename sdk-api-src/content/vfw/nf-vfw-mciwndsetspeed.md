---
UID: NF:vfw.MCIWndSetSpeed
title: MCIWndSetSpeed macro (vfw.h)
description: The MCIWndSetSpeed macro sets the playback speed of an MCI device. You can use this macro or explicitly send the MCIWNDM_SETSPEED message.
helpviewer_keywords: ["MCIWndSetSpeed","MCIWndSetSpeed macro [Windows Multimedia]","_win32_MCIWndSetSpeed","multimedia.mciwndsetspeed","vfw/MCIWndSetSpeed"]
old-location: multimedia\mciwndsetspeed.htm
tech.root: Multimedia
ms.assetid: aaf45d2f-3f6c-4b87-82fe-3fca3f36f57d
ms.date: 12/05/2018
ms.keywords: MCIWndSetSpeed, MCIWndSetSpeed macro [Windows Multimedia], _win32_MCIWndSetSpeed, multimedia.mciwndsetspeed, vfw/MCIWndSetSpeed
f1_keywords:
- vfw/MCIWndSetSpeed
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
- MCIWndSetSpeed
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MCIWndSetSpeed macro


## -description



The <b>MCIWndSetSpeed</b> macro sets the playback speed of an MCI device. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mciwndm-setspeed">MCIWNDM_SETSPEED</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param iSpeed

Playback speed. Specify 1000 for normal speed, larger values for faster speeds, and smaller values for slower speeds. 

