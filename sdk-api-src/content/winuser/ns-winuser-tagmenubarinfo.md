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

# tagMENUBARINFO structure


## -description


Contains menu bar information.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes. The caller must set this to <code>sizeof(MENUBARINFO)</code>. 


### -field rcBar

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a></b>

The coordinates of the menu bar, popup menu, or menu item. 


### -field hMenu

Type: <b>HMENU</b>

A handle to the menu bar or popup menu. 


### -field hwndMenu

Type: <b>HWND</b>

A handle to the submenu. 


### -field fBarFocused

Type: <b>BOOL</b>

If the menu bar or popup menu has the focus, this member is <b>TRUE</b>. Otherwise, the member is <b>FALSE</b>. 


### -field fFocused

Type: <b>BOOL</b>

If the menu item has the focus, this member is <b>TRUE</b>. Otherwise, the member is <b>FALSE</b>. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/552868df-9641-4584-bbd1-89c8c5806a68">GetMenuBarInfo</a>



<a href="https://msdn.microsoft.com/f00c0b76-fabb-4451-bd4e-30b465d4d235">Menus</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>



<b>Reference</b>
 

 

