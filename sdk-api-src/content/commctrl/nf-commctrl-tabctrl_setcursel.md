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

# TabCtrl_SetCurSel macro


## -description


Selects a tab in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/cf709d8c-c522-47c8-8ff3-463dc8e924b5">TCM_SETCURSEL</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param i

TBD






#### - iItem

Type: <b>int</b>

Index of the tab to select. 


## -remarks



A tab control does not send a <a href="https://msdn.microsoft.com/ec7b1bd3-8932-4418-9eed-ecb7c748e4dd">TCN_SELCHANGING</a> or <a href="https://msdn.microsoft.com/f40e30f6-169b-4381-a300-12c3befb5fc5">TCN_SELCHANGE</a> notification code when a tab is selected using the <a href="https://msdn.microsoft.com/cf709d8c-c522-47c8-8ff3-463dc8e924b5">TCM_SETCURSEL</a> message. 



