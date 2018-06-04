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

# MCIWndGetLength macro


## -description



The <b>MCIWndGetLength</b> macro retrieves the length of the content or file currently used by an MCI device. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f">MCIWNDM_GETLENGTH</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


## -remarks



This value added to the value returned for the <a href="https://msdn.microsoft.com/fe9346b8-e917-4bbc-9df5-3b0b5c2de306">MCIWndGetStart</a> macro equals the end of the content.




## -see-also




<a href="https://msdn.microsoft.com/bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f">MCIWNDM_GETLENGTH</a>



<a href="https://msdn.microsoft.com/fe9346b8-e917-4bbc-9df5-3b0b5c2de306">MCIWndGetStart</a>
 

 

