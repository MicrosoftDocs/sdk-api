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

# MCIWndSetPalette macro


## -description



The <b>MCIWndSetPalette</b> macro sends a palette handle to the MCI device associated with the MCIWnd window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/d2399cb7-d83c-465c-b02f-e6a016c28ae3">MCIWNDM_SETPALETTE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param hpal

Palette handle. 

