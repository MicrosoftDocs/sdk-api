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

# ListView_GetISearchString macro


## -description


Gets the incremental search string of a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/e953c4a0-0556-4987-8abf-3276e787fe49">LVM_GETISEARCHSTRING</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param lpsz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

A pointer to a buffer that receives the incremental search string. To just retrieve the length of the string, set <i>lpsz</i> to <b>NULL</b>. 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



The incremental search string is the character sequence that the user types while the list view has the input focus. Each time the user types a character, the system appends the character to the search string and then searches for a matching item. If the system finds a match, it selects the item and, if necessary, scrolls it into view. 

A time-out period is associated with each character that the user types. If the time-out period elapses before the user types another character, the incremental search string is reset. 

Make sure that the buffer is large enough to hold the string. If it is too small, an immediate invalid page fault will result. 



