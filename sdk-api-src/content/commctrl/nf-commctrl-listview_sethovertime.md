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

# ListView_SetHoverTime macro


## -description


Sets the amount of time that the mouse cursor must hover over an item before it is selected. You can use this macro or send the <a href="https://msdn.microsoft.com/454fbc38-f7fd-4dea-b223-56003b88528f">LVM_SETHOVERTIME</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


### -param dwHoverTimeMs

TBD






#### - dwHoverTime

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The new amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected. If this value is (<b>DWORD</b>)-1, then the hover time is set to the default hover time. 


## -remarks



The hover time only affects list-view controls that have the <a href="Extended_list_view_styles.htm">LVS_EX_TRACKSELECT</a>, <a href="Extended_list_view_styles.htm">LVS_EX_ONECLICKACTIVATE</a>, or <a href="Extended_list_view_styles.htm">LVS_EX_TWOCLICKACTIVATE</a> extended list-view style. 



