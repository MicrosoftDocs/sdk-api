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

# tagSMINFO structure


## -description


Contains information about an item from a menu band.


## -struct-fields




### -field dwMask

Type: <b>DWORD</b>

Flags that specify which of the other three members are valid.



#### SMIM_TYPE

The <b>dwType</b> member contains valid information.



#### SMIM_FLAGS

The <b>dwFlags</b> member contains valid information.



#### SMIM_ICON

The <b>iIcon</b> member contains valid information.


### -field dwType

Type: <b>DWORD</b>

A flag that indicates whether the item is a string or a separator.



#### SMIT_SEPARATOR

A menu separator.



#### SMIT_STRING

A menu string.


### -field dwFlags

Type: <b>DWORD</b>

Flags that contain information about the item and how it should be displayed.



#### SMIF_ICON

Show an icon.



#### SMIF_ACCELERATOR

Underline the character marked with an ampersand.



#### SMIF_DROPTARGET

The item is a drop target.



#### SMIF_SUBMENU

The item has a submenu.



#### SMIF_VOLATILE

Not used.



#### SMIF_CHECKED

The item has a check beside it.



#### SMIF_DROPCASCADE

The item can cascade during a drag-drop operation.



#### SMIF_HIDDEN

Do not display the item.



#### SMIF_DISABLED

Make the item unselectable. It will be displayed in gray and will not respond to user actions.



#### SMIF_TRACKPOPUP

Use <a href="https://msdn.microsoft.com/2e1e4648-e3fd-4d9a-a558-de7b030e3d75">TrackPopupMenu</a> to create the pop-up menu.



#### SMIF_DEMOTED

Display the item in a "demoted"" state.



#### SMIF_ALTSTATE

Display the item in an "altered" state.



#### SMIF_DRAGNDROP

Make the item sensitive to a hovering cursor. If the cursor remains over the item for a sufficient duration, it will execute as if the user had clicked the item.



#### SMIF_NEW

This item is newly installed or should be brought to the user's attention.


### -field iIcon

Type: <b>int</b>

When <b>SMIF_ICON</b> is set, the index of the requested icon in the toolbar image list.

