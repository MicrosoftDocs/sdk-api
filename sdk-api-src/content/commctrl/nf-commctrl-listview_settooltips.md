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

# ListView_SetToolTips macro


## -description


Sets the tooltip control that the list-view control will use to display tooltips. You can use this macro or send the <a href="https://msdn.microsoft.com/5b4335a4-e9f0-4b13-b00b-516af3b60bf1">LVM_SETTOOLTIPS</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param hwndNewHwnd

TBD






#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - hwndToolTip

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the tooltip control to be set. 


## -see-also




<a href="https://msdn.microsoft.com/3d8277a6-e35d-4b07-9817-d13b42a66fe6">ListView_GetToolTips</a>
 

 

