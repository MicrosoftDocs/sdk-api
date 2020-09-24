---
UID: NS:shobjidl_core.tagSMINFO
title: SMINFO (shobjidl_core.h)
description: Contains information about an item from a menu band.
helpviewer_keywords: ["*PSMINFO","PSMINFO","PSMINFO structure pointer [Windows Shell]","SMIF_ACCELERATOR","SMIF_ALTSTATE","SMIF_CHECKED","SMIF_DEMOTED","SMIF_DISABLED","SMIF_DRAGNDROP","SMIF_DROPCASCADE","SMIF_DROPTARGET","SMIF_HIDDEN","SMIF_ICON","SMIF_NEW","SMIF_SUBMENU","SMIF_TRACKPOPUP","SMIF_VOLATILE","SMIM_FLAGS","SMIM_ICON","SMIM_TYPE","SMINFO","SMINFO structure [Windows Shell]","SMIT_SEPARATOR","SMIT_STRING","_win32_SMINFO","shell.SMINFO","shobjidl_core/PSMINFO","shobjidl_core/SMINFO","tagSMINFO"]
old-location: shell\SMINFO.htm
tech.root: shell
ms.assetid: aaa6ee05-7236-4b68-9d93-4848c4fe693d
ms.date: 12/05/2018
ms.keywords: '*PSMINFO, PSMINFO, PSMINFO structure pointer [Windows Shell], SMIF_ACCELERATOR, SMIF_ALTSTATE, SMIF_CHECKED, SMIF_DEMOTED, SMIF_DISABLED, SMIF_DRAGNDROP, SMIF_DROPCASCADE, SMIF_DROPTARGET, SMIF_HIDDEN, SMIF_ICON, SMIF_NEW, SMIF_SUBMENU, SMIF_TRACKPOPUP, SMIF_VOLATILE, SMIM_FLAGS, SMIM_ICON, SMIM_TYPE, SMINFO, SMINFO structure [Windows Shell], SMIT_SEPARATOR, SMIT_STRING, _win32_SMINFO, shell.SMINFO, shobjidl_core/PSMINFO, shobjidl_core/SMINFO, tagSMINFO'
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SMINFO, *PSMINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSMINFO
 - shobjidl_core/tagSMINFO
 - PSMINFO
 - shobjidl_core/PSMINFO
 - SMINFO
 - shobjidl_core/SMINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shobjidl_core.h
api_name:
 - SMINFO
---

# SMINFO structure


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

Use <a href="/windows/desktop/api/winuser/nf-winuser-trackpopupmenu">TrackPopupMenu</a> to create the pop-up menu.



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