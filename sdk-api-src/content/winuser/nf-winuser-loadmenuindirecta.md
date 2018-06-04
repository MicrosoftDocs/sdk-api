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

# LoadMenuIndirectA function


## -description


Loads the specified menu template in memory. 


## -parameters




### -param lpMenuTemplate [in]

Type: <b>const MENUTEMPLATE*</b>

A pointer to a menu template or an extended menu template. A menu template consists of a <a href="https://msdn.microsoft.com/7dd21370-9e26-4086-9ba1-98e79966c336">MENUITEMTEMPLATEHEADER</a> structure followed by one or more contiguous <a href="https://msdn.microsoft.com/9329aee3-83be-4409-98f4-e135f39c0f01">MENUITEMTEMPLATE</a> structures. An extended menu template consists of a <a href="https://msdn.microsoft.com/df763349-7127-482e-8613-74e68addde5d">MENUEX_TEMPLATE_HEADER</a> structure followed by one or more contiguous <a href="https://msdn.microsoft.com/f6e2fd0a-16b8-48e3-8597-341085a7adbd">MENUEX_TEMPLATE_ITEM</a> structures. 


## -returns



Type: <b>HMENU</b>

If the function succeeds, the return value is a handle to the menu.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



For both the ANSI and the Unicode version of this function, the strings in the <a href="https://msdn.microsoft.com/9329aee3-83be-4409-98f4-e135f39c0f01">MENUITEMTEMPLATE</a> structure must be Unicode strings. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/806297e1-0ee4-4471-a98a-598c1b48c0de">LoadMenu</a>



<a href="https://msdn.microsoft.com/df763349-7127-482e-8613-74e68addde5d">MENUEX_TEMPLATE_HEADER</a>



<a href="https://msdn.microsoft.com/f6e2fd0a-16b8-48e3-8597-341085a7adbd">MENUEX_TEMPLATE_ITEM</a>



<a href="https://msdn.microsoft.com/9329aee3-83be-4409-98f4-e135f39c0f01">MENUITEMTEMPLATE</a>



<a href="https://msdn.microsoft.com/7dd21370-9e26-4086-9ba1-98e79966c336">MENUITEMTEMPLATEHEADER</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<b>Reference</b>
 

 

