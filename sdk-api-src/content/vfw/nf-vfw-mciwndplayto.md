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

# MCIWndPlayTo macro


## -description



The <b>MCIWndPlayTo</b> macro plays the content of an MCI device from the current position to the specified ending location or until another command stops playback. If the specified ending location is beyond the end of the content, playback stops at the end of the content. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/ed940ee7-7b96-47da-99d3-6697f8a2e3d5">MCIWNDM_PLAYTO</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lPos

Ending location. The units for the ending location depend on the current time format. 


## -remarks



You can also specify both a starting and ending location for playback by using the <a href="https://msdn.microsoft.com/a592c28c-322f-4fd1-90e9-632703bf40c1">MCIWndPlayFromTo</a> macro.



