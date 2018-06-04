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

# ListView_DeleteAllItems macro


## -description


Removes all items from a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/816bf565-79e9-4f5d-b5b4-5cdecce8a61c">LVM_DELETEALLITEMS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



When a list-view control receives the <a href="https://msdn.microsoft.com/816bf565-79e9-4f5d-b5b4-5cdecce8a61c">LVM_DELETEALLITEMS</a> message, it sends the <a href="https://msdn.microsoft.com/e4a219cf-4af9-4d02-8810-f576ba658177">LVN_DELETEALLITEMS</a> notification code to its parent window. 



