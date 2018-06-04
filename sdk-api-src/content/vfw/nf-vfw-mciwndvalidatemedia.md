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

# MCIWndValidateMedia macro


## -description



The <b>MCIWndValidateMedia</b> macro updates the starting and ending locations of the content, the current position in the content, and the trackbar according to the current time format. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/98ac6227-fc90-4276-8e26-2bd005e35dc6">MCIWNDM_VALIDATEMEDIA</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


## -remarks



Typically, you should not need to use this macro; however, if your application changes the time format of a device without using MCIWnd; the starting and ending locations of the content, as well as the trackbar, continue to use the old format. You can use this macro to update these values.



