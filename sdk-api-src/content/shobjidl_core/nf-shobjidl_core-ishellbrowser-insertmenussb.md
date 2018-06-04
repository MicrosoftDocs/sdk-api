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

# IShellBrowser::InsertMenusSB


## -description


Allows the container to insert its menu groups into the composite menu that is displayed when an extended namespace is being viewed or used.


## -parameters




### -param hmenuShared

Type: <b>HMENU</b>

A handle to an empty menu.


### -param lpMenuWidths

Type: <b>LPOLEMENUGROUPWIDTHS</b>

The address of an <a href="https://msdn.microsoft.com/e6ad4ab7-0e53-4fad-8f2e-a0ff7b376815">OLEMENUGROUPWIDTHS</a> array of six <b>LONG</b> values. The container fills in elements 0, 2, and 4 to reflect the number of menu elements it provided in the File, View, and Window menu groups.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or a COM-defined error value otherwise.




## -remarks



This method is similar to the <a href="https://msdn.microsoft.com/659ea109-c2c1-4146-aed2-60b1ce853d89">IOleInPlaceFrame::InsertMenus</a> method. Windows Explorer puts <b>File</b> and <b>Edit</b> drop-down menus in the File menu group, <b>View</b> and <b>Tools</b> menus in the Container menu group, and a <b>Help</b> menu in the Window menu group. Each drop-down menu will have a unique identifier, FCIDM_MENU_FILE/EDIT/VIEW/TOOLS/HELP. The view is allowed to insert menu items into those submenus by their identifiers, which is different from OLE's in-place activation mechanism. The command identifiers for menus that the view inserts into either Windows Explorer's submenus or its own submenus must be between <b>FCIDM_SHVIEWFIRST</b> and <b>FCIDM_SHVIEWLAST</b>.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
This method is called by namespace extensions when they are first being activated so they can insert their menus into the frame-level user interface.

The object application asks the container to add its menus to the menu specified in the <i>hmenuShared</i> parameter and to set the group counts in the <a href="https://msdn.microsoft.com/e6ad4ab7-0e53-4fad-8f2e-a0ff7b376815">OLEMENUGROUPWIDTHS</a> array pointed to by the <i>lpMenuWidths</i> parameter. The object application then adds its own menus and counts. Objects can call the <a href="https://msdn.microsoft.com/659ea109-c2c1-4146-aed2-60b1ce853d89">IOleInPlaceFrame::InsertMenus</a> method as many times as necessary to build up the composite menus. The container should use the initial menu handle associated with the composite menu for all items in the drop-down menus.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
For <a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a> implementations, the menu identifiers must be in the range of <b>FCIDM_BROWSERFIRST</b> to <b>FCIDM_BROWSERLAST</b>.



