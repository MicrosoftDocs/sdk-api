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

# MCIWndPlayFrom macro


## -description



The <b>MCIWndPlayFrom</b> macro plays the content of an MCI device from the specified location to the end of the content or until another command stops playback. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/1c47f8eb-2a1b-4671-a9f8-fd6d59a5c7c6">MCIWNDM_PLAYFROM</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lPos

Starting location. The units for the starting location depend on the current time format. 


## -remarks



You can also specify both a starting and ending location for playback by using the <a href="https://msdn.microsoft.com/a592c28c-322f-4fd1-90e9-632703bf40c1">MCIWndPlayFromTo</a> macro.



