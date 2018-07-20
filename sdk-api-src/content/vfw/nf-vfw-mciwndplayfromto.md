---
UID: NF:vfw.MCIWndPlayFromTo
title: MCIWndPlayFromTo macro
author: windows-sdk-content
description: The MCIWndPlayFromTo macro plays a portion of content between specified starting and ending locations.
old-location: multimedia\mciwndplayfromto.htm
old-project: Multimedia
ms.assetid: a592c28c-322f-4fd1-90e9-632703bf40c1
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: MCIWndPlayFromTo, MCIWndPlayFromTo macro [Windows Multimedia], _win32_MCIWndPlayFromTo, multimedia.mciwndplayfromto, vfw/MCIWndPlayFromTo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
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
tech.root: 
req.typenames: VS_FIXEDFILEINFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - MCIWndPlayFromTo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# MCIWndPlayFromTo macro


## -description



The <b>MCIWndPlayFromTo</b> macro plays a portion of content between specified starting and ending locations. This macro seeks to the specified point to begin playback, then plays the content to the specified ending location. This macro is defined using the <a href="https://msdn.microsoft.com/96d42e1a-03d5-4007-95d8-0e4b8d2018d5">MCIWndSeek</a> and <a href="https://msdn.microsoft.com/49048776-85bd-43ac-a5a0-414a26a6a533">MCIWndPlayTo</a> macros, which in turn use the <a href="https://msdn.microsoft.com/5ffab964-a28d-4dc2-ac04-da501cd34d24">MCI_SEEK</a> command and the <a href="https://msdn.microsoft.com/ed940ee7-7b96-47da-99d3-6697f8a2e3d5">MCIWNDM_PLAYTO</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lStart

Position to seek; it is also the starting location. 


### -param lEnd

Ending location. 


## -remarks



The units for the seek position depend on the current time format.



