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

# tagHELPINFO structure


## -description


Contains information about an item for which context-sensitive Help has been requested.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The structure size, in bytes.


### -field iContextType

Type: <b>int</b>

The type of context for which Help is requested. This member can be one of the following values.



#### HELPINFO_MENUITEM

Help requested for a menu item.



#### HELPINFO_WINDOW

Help requested for a control or window.


### -field iCtrlId

Type: <b>int</b>

The identifier of the window or control if <b>iContextType</b> is <b>HELPINFO_WINDOW</b>, or identifier of the menu item if <b>iContextType</b> is <b>HELPINFO_MENUITEM</b>.


### -field hItemHandle

Type: <b>HANDLE</b>

The identifier of the child window or control if <b>iContextType</b> is <b>HELPINFO_WINDOW</b>, or identifier of the associated menu if <b>iContextType</b> is <b>HELPINFO_MENUITEM</b>.


### -field dwContextId

Type: <b>DWORD</b>

The help context identifier of the window or control.


### -field MousePos

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure that contains the screen coordinates of the mouse cursor. This is useful for providing Help based on the position of the mouse cursor.

