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

# TabCtrl_GetToolTips macro


## -description


Retrieves the handle to the tooltip control associated with a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/d7dcca4f-8629-4eeb-844f-b3171438f528">TCM_GETTOOLTIPS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


## -remarks



A tab control creates a tooltip control if it has the <a href="Tab_Control_Styles.htm">TCS_TOOLTIPS</a>. You can also assign a tooltip control to a tab control by using the <a href="https://msdn.microsoft.com/c1b173b1-9da6-441a-a2b6-3875e2c343f8">TCM_SETTOOLTIPS</a> message. 



