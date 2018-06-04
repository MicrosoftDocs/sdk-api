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

# ListView_GetStringWidth macro


## -description


Determines the width of a specified string using the specified list-view control's current font. You can use this macro or send the <a href="https://msdn.microsoft.com/ffe97640-d4b6-45ae-be5d-71fed69c2026">LVM_GETSTRINGWIDTH</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param psz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

A pointer to a null-terminated string. 


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



The <b>ListView_GetStringWidth</b> macro returns the exact width, in pixels, of the specified string. If you use the returned string width as the column width in a call to the <a href="https://msdn.microsoft.com/0eb0c038-8f94-49d7-a783-23adef02b4c2">ListView_SetColumnWidth</a> macro, the string will be truncated. To retrieve the column width that can contain the string without truncating it, you must add padding to the returned string width. 



