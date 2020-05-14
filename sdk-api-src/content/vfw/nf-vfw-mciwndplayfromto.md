---
UID: NF:vfw.MCIWndPlayFromTo
title: MCIWndPlayFromTo macro (vfw.h)
description: The MCIWndPlayFromTo macro plays a portion of content between specified starting and ending locations.helpviewer_keywords: ["MCIWndPlayFromTo","MCIWndPlayFromTo macro [Windows Multimedia]","_win32_MCIWndPlayFromTo","multimedia.mciwndplayfromto","vfw/MCIWndPlayFromTo"]
old-location: multimedia\mciwndplayfromto.htm
tech.root: Multimedia
ms.assetid: a592c28c-322f-4fd1-90e9-632703bf40c1
ms.date: 12/05/2018
ms.keywords: MCIWndPlayFromTo, MCIWndPlayFromTo macro [Windows Multimedia], _win32_MCIWndPlayFromTo, multimedia.mciwndplayfromto, vfw/MCIWndPlayFromTo
f1_keywords:
- vfw/MCIWndPlayFromTo
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
- MCIWndPlayFromTo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MCIWndPlayFromTo macro


## -description



The <b>MCIWndPlayFromTo</b> macro plays a portion of content between specified starting and ending locations. This macro seeks to the specified point to begin playback, then plays the content to the specified ending location. This macro is defined using the <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-mciwndseek">MCIWndSeek</a> and <a href="https://docs.microsoft.com/windows/desktop/api/vfw/nf-vfw-mciwndplayto">MCIWndPlayTo</a> macros, which in turn use the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mci-seek">MCI_SEEK</a> command and the <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mciwndm-playto">MCIWNDM_PLAYTO</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lStart

Position to seek; it is also the starting location. 


### -param lEnd

Ending location. 


## -remarks



The units for the seek position depend on the current time format.



