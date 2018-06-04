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

# MCIWndNew macro


## -description



The <b>MCIWndNew</b> macro creates a new file for the current MCI device. You can use this macro or explicitly send the <a href="https://msdn.microsoft.com/18b2340d-8303-415a-867f-bd346034db2a">MCIWNDM_NEW</a> message.




## -parameters




### -param hwnd

Handle of the MCIWnd window. 


### -param lp

Pointer to a buffer containing the name of the MCI device that will use the file. 


## -see-also




<a href="https://msdn.microsoft.com/18b2340d-8303-415a-867f-bd346034db2a">MCIWNDM_NEW</a>
 

 

