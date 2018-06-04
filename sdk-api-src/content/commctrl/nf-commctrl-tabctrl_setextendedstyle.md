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

# TabCtrl_SetExtendedStyle macro


## -description


Sets the extended styles that the tab control will use. You can use this macro or send the <a href="https://msdn.microsoft.com/96ccebe1-2836-4198-8cd7-858401562c21">TCM_SETEXTENDEDSTYLE</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param dw

TBD






#### - dwExStyle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Value that contains the new tab control extended styles. This value is a combination of tab control <a href="https://msdn.microsoft.com/24294037-598c-4fcd-8a7c-8647ccfb1d81">extended styles</a>. 


#### - hwndTab

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 

