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

# MCIWndChangeStyles macro


## -description



The <b>MCIWndChangeStyles</b> macro changes the styles used by the MCIWnd window. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/9074c21a-e49f-4089-a6d2-af8d513cb632">MCIWNDM_CHANGESTYLES</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param mask

Mask that identifies the styles that can change. This mask is the bitwise OR operator of all styles that will be permitted to change. 


### -param value

New style settings for the window. Specify zero for this parameter to turn off all styles identified in the mask. For a list of the available styles, see the MCIWndCreate function. 


## -remarks



For an example of using <b>MCIWndChangeStyles</b>, see <a href="https://msdn.microsoft.com/f5a7ef22-993c-4aab-bab0-2700289da7a7">Pausing and Resuming Playback</a>.




## -see-also




<a href="https://msdn.microsoft.com/9074c21a-e49f-4089-a6d2-af8d513cb632">MCIWNDM_CHANGESTYLES</a>
 

 

