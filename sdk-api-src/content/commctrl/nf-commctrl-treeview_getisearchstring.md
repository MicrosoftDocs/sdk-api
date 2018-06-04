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

# TreeView_GetISearchString macro


## -description


Retrieves the incremental search string for a tree-view control. The tree-view control uses the incremental search string to select an item based on characters typed by the user. You can use this macro or send the <a href="https://msdn.microsoft.com/71f9a9b6-e124-4655-80fc-dd23f441496d">TVM_GETISEARCHSTRING</a> message explicitly. 


## -parameters




### -param hwndTV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tree-view control. 


### -param lpsz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Pointer to the buffer that receives the incremental search string. 


## -remarks



<b>Security Warning:  </b>Using this macro incorrectly might compromise the security of your program. You must allocate a large enough buffer to hold the string. First call the macro passing <b>NULL</b> in <i>lpsz</i>. This returns the number of characters, excluding <b>NULL</b>, that are required. Then call the macro a second time to retrieve the string.  You should review <a href="https://msdn.microsoft.com/d5396fa1-452e-40e1-beaf-ae04690048f1">Security Considerations: Microsoft Windows Controls</a> before continuing.

If the tree-view control is not in incremental search mode, the return value is zero. 



