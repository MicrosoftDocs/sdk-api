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

# TabCtrl_HitTest macro


## -description


Determines which tab, if any, is at a specified screen position. You can use this macro or send the <a href="https://msdn.microsoft.com/0334f616-8d39-4460-a7f8-692a9ffab012">TCM_HITTEST</a> message explicitly. 


## -parameters




### -param hwndTC

TBD


### -param pinfo

Type: <b>LPTCHITTESTINFO</b>

Pointer to a <a href="https://msdn.microsoft.com/7d3de7be-bf10-474e-a596-8de7a4c2a179">TCHITTESTINFO</a> structure that specifies the screen position to test. 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 

