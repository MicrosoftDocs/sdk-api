---
UID: NF:shobjidl_core.IShellBrowser.InsertMenusSB
title: IShellBrowser::InsertMenusSB (shobjidl_core.h)
description: Allows the container to insert its menu groups into the composite menu that is displayed when an extended namespace is being viewed or used.
helpviewer_keywords: ["IShellBrowser interface [Windows Shell]","InsertMenusSB method","IShellBrowser.InsertMenusSB","IShellBrowser::InsertMenusSB","InsertMenusSB","InsertMenusSB method [Windows Shell]","InsertMenusSB method [Windows Shell]","IShellBrowser interface","_win32_IShellBrowser_InsertMenusSB","shell.IShellBrowser_InsertMenusSB","shobjidl_core/IShellBrowser::InsertMenusSB"]
old-location: shell\IShellBrowser_InsertMenusSB.htm
tech.root: shell
ms.assetid: 62cbb593-7459-4a4f-96a2-3ec2287e6a26
ms.date: 12/05/2018
ms.keywords: IShellBrowser interface [Windows Shell],InsertMenusSB method, IShellBrowser.InsertMenusSB, IShellBrowser::InsertMenusSB, InsertMenusSB, InsertMenusSB method [Windows Shell], InsertMenusSB method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_InsertMenusSB, shell.IShellBrowser_InsertMenusSB, shobjidl_core/IShellBrowser::InsertMenusSB
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellBrowser::InsertMenusSB
 - shobjidl_core/IShellBrowser::InsertMenusSB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellBrowser.InsertMenusSB
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

The address of an <a href="/windows/desktop/api/oleidl/ns-oleidl-olemenugroupwidths">OLEMENUGROUPWIDTHS</a> array of six <b>LONG</b> values. The container fills in elements 0, 2, and 4 to reflect the number of menu elements it provided in the File, View, and Window menu groups.

## -returns

Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or a COM-defined error value otherwise.

## -remarks

This method is similar to the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-insertmenus">IOleInPlaceFrame::InsertMenus</a> method. Windows Explorer puts <b>File</b> and <b>Edit</b> drop-down menus in the File menu group, <b>View</b> and <b>Tools</b> menus in the Container menu group, and a <b>Help</b> menu in the Window menu group. Each drop-down menu will have a unique identifier, FCIDM_MENU_FILE/EDIT/VIEW/TOOLS/HELP. The view is allowed to insert menu items into those submenus by their identifiers, which is different from OLE's in-place activation mechanism. The command identifiers for menus that the view inserts into either Windows Explorer's submenus or its own submenus must be between <b>FCIDM_SHVIEWFIRST</b> and <b>FCIDM_SHVIEWLAST</b>.

<h3><a id="Notes_to_Calling_Applications"></a><a id="notes_to_calling_applications"></a><a id="NOTES_TO_CALLING_APPLICATIONS"></a>Notes to Calling Applications</h3>
This method is called by namespace extensions when they are first being activated so they can insert their menus into the frame-level user interface.

The object application asks the container to add its menus to the menu specified in the <i>hmenuShared</i> parameter and to set the group counts in the <a href="/windows/desktop/api/oleidl/ns-oleidl-olemenugroupwidths">OLEMENUGROUPWIDTHS</a> array pointed to by the <i>lpMenuWidths</i> parameter. The object application then adds its own menus and counts. Objects can call the <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleinplaceframe-insertmenus">IOleInPlaceFrame::InsertMenus</a> method as many times as necessary to build up the composite menus. The container should use the initial menu handle associated with the composite menu for all items in the drop-down menus.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
For <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a> implementations, the menu identifiers must be in the range of <b>FCIDM_BROWSERFIRST</b> to <b>FCIDM_BROWSERLAST</b>.