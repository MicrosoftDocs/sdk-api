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

# ListView_GetBkImage macro


## -description


Gets the background image in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/db0e8f31-746a-4a16-b689-68da696e3657">LVM_GETBKIMAGE</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param plvbki

Type: <b>LPLVBKIMAGE</b>

A pointer to a <a href="https://msdn.microsoft.com/d8b35356-d112-43e5-b1ad-7fb945c84e33">LVBKIMAGE</a> structure that will receive the background image information. 


#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -see-also




<a href="https://msdn.microsoft.com/8ee481c7-e114-45bd-9082-16d756152e54">ListView_SetBkImage</a>
 

 

