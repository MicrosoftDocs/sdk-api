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

# Pager_SetBkColor macro


## -description


Sets the current background color for the pager control. You can use this macro or send the <a href="https://msdn.microsoft.com/720a25d7-3854-4f28-b227-bafab7b1e8c9">PGM_SETBKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param clr

TBD






#### - clrBk

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

<b>COLORREF</b> value that contains the new background color of the pager control. 


#### - hwndPager

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the pager control. 


## -remarks



By default, the pager control will use the system button face color as the background color. This is the same color that can be retrieved by calling <a href="https://msdn.microsoft.com/07a1d8e3-eae8-40ab-9d0f-4efa9fac0117">GetSysColorBrush</a> with COLOR_BTNFACE. 



