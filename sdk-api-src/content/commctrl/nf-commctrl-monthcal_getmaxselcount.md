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

# MonthCal_GetMaxSelCount macro


## -description


Retrieves the maximum date range that can be selected in a month calendar control. You can use this macro or send the <a href="https://msdn.microsoft.com/34204231-3a3c-4eba-913d-b0c27769c338">MCM_GETMAXSELCOUNT</a> message explicitly. 


## -parameters




### -param hmc

TBD






#### - hwndMC

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to a month calendar control. 


## -remarks



You can change the maximum date range that can be selected by using the <a href="https://msdn.microsoft.com/190453ab-e53b-4db7-82c1-f9d50188ad39">MCM_SETMAXSELCOUNT</a> message. 



