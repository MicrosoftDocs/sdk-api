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

# MCIWndRealize macro


## -description



The <b>MCIWndRealize</b> macro controls how an MCI window realized in the foreground or background. This macro also causes the palette for the MCI window to be realized in the process. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/fe8803b5-3500-44b4-97f7-784bedf0b362">MCIWNDM_REALIZE</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param fBkgnd

Background flag. Specify <b>TRUE</b> for this parameter for the window to be realized in the background or <b>FALSE</b> if the window can be realized in the foreground. 


## -remarks



A common use for <b>MCIWndRealize</b> is to coordinate palette ownership between an MCI control and the application that contains it. The application can have the MCI window realize in the background and realize its own palette in the foreground.

If your application contains an MCI control, but does not need to realize its palette, you can use this macro to handle the WM_PALETTECHANGED and WM_QUERYNEWPALETTE messages, instead of using <b>RealizePalette</b>. However, it is usually easier to call the <b>SendMessage</b> function to forward the message to the MCIWnd window, which will automatically realize the palette.



