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

# MCIWndSetTimeFormat macro


## -description



The <b>MCIWndSetTimeFormat</b> macro sets the time format of an MCI device. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/7de82094-6d35-44fd-88e7-ebd18a558cfd">MCIWNDM_SETTIMEFORMAT</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to a buffer containing the null-terminated string indicating the time format. Specify "frames" to set the time format to frames, or "ms" to set the time format to milliseconds. 


## -remarks



An application can specify time formats other than frames or milliseconds as long as the formats are supported by the MCI device. Noncontinuous formats, such as tracks and SMPTE, can cause the trackbar to behave erratically. For these time formats, you might want to turn off the toolbar by using the <a href="https://msdn.microsoft.com/d87da0b0-4217-421d-a9d5-03602fb2b477">MCIWndChangeStyles</a> macro and specifying the MCIWNDF_NOPLAYBAR window style.

If you want to set the time format to frames or milliseconds, you can also use the <b>MCIWndUseFrames</b> or <b>MCIWndUseTime</b> macro. For a list of time formats, see the <b>MCIWndGetTimeFormat</b> macro.



