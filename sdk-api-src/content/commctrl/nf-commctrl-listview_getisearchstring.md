---
UID: NF:commctrl.ListView_GetISearchString
title: ListView_GetISearchString macro
author: windows-sdk-content
description: Gets the incremental search string of a list-view control. You can use this macro or send the LVM_GETISEARCHSTRING message explicitly.
old-location: controls\ListView_GetISearchString.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getisearchstring.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ListView_GetISearchString, ListView_GetISearchString macro [Windows Controls], _win32_ListView_GetISearchString, _win32_ListView_GetISearchString_cpp, commctrl/ListView_GetISearchString, controls.ListView_GetISearchString, controls._win32_ListView_GetISearchString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_GetISearchString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetISearchString macro


## -description


Gets the incremental search string of a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/e953c4a0-0556-4987-8abf-3276e787fe49">LVM_GETISEARCHSTRING</a> message explicitly. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param lpsz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPSTR</a></b>

A pointer to a buffer that receives the incremental search string. To just retrieve the length of the string, set <i>lpsz</i> to <b>NULL</b>. 


## -remarks



The incremental search string is the character sequence that the user types while the list view has the input focus. Each time the user types a character, the system appends the character to the search string and then searches for a matching item. If the system finds a match, it selects the item and, if necessary, scrolls it into view. 

A time-out period is associated with each character that the user types. If the time-out period elapses before the user types another character, the incremental search string is reset. 

Make sure that the buffer is large enough to hold the string. If it is too small, an immediate invalid page fault will result. 



