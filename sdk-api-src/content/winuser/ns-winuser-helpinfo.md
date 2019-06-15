---
UID: NS:winuser.tagHELPINFO
title: HELPINFO (winuser.h)
author: windows-sdk-content
description: Contains information about an item for which context-sensitive Help has been requested.
old-location: shell\HELPINFO_str.htm
tech.root: shell
ms.assetid: 8320fb68-294b-487b-ab5a-6611bb57cff0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPHELPINFO, HELPINFO, HELPINFO structure [Windows Shell], HELPINFO_MENUITEM, HELPINFO_WINDOW, LPHELPINFO, LPHELPINFO structure pointer [Windows Shell], _win32_HELPINFO_str, _win32_helpinfo_str_cpp, shell.HELPINFO_str, tagHELPINFO, winuser/HELPINFO, winuser/LPHELPINFO"
ms.topic: struct
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Winuser.h
api_name:
 - HELPINFO
product: Windows
targetos: Windows
req.typenames: HELPINFO, *LPHELPINFO
req.redist: 
ms.custom: 19H1
---

# HELPINFO structure


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

Type: <b><a href="https://docs.microsoft.com/previous-versions//dd162805(v=vs.85)">POINT</a></b>

The <a href="https://docs.microsoft.com/previous-versions//dd162805(v=vs.85)">POINT</a> structure that contains the screen coordinates of the mouse cursor. This is useful for providing Help based on the position of the mouse cursor.

