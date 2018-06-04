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

# MCIWndSetRepeat macro


## -description



The <b>MCIWndSetRepeat</b> macro sets the repeat flag associated with continuous playback. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/9a8da201-9ce8-4b6c-8b76-cd9e1356c75d">MCIWNDM_SETREPEAT</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param f

New state of the repeat flag. Specify <b>TRUE</b> to turn on continuous playback. 


## -remarks



The <b>MCIWndSetRepeat</b> macro only affects playback that the user initiates by hitting the play button on the toolbar. It will not affect playback started with the <b>MCIWndPlay</b> macro.

Currently, MCIAVI is the only device that supports continuous playback.



