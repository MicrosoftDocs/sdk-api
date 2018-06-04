---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



