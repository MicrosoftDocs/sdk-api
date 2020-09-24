---
UID: NF:shobjidl_core.IShellBrowser.SetToolbarItems
title: IShellBrowser::SetToolbarItems (shobjidl_core.h)
description: Adds toolbar items to Windows Explorer's toolbar.
helpviewer_keywords: ["FCT_ADDTOEND","FCT_CONFIGABLE","FCT_MERGE","IShellBrowser interface [Windows Shell]","SetToolbarItems method","IShellBrowser.SetToolbarItems","IShellBrowser::SetToolbarItems","SetToolbarItems","SetToolbarItems method [Windows Shell]","SetToolbarItems method [Windows Shell]","IShellBrowser interface","_win32_IShellBrowser_SetToolbarItems","shell.IShellBrowser_SetToolbarItems","shobjidl_core/IShellBrowser::SetToolbarItems"]
old-location: shell\IShellBrowser_SetToolbarItems.htm
tech.root: shell
ms.assetid: 4ff141d3-e175-464a-9869-317d547e7489
ms.date: 12/05/2018
ms.keywords: FCT_ADDTOEND, FCT_CONFIGABLE, FCT_MERGE, IShellBrowser interface [Windows Shell],SetToolbarItems method, IShellBrowser.SetToolbarItems, IShellBrowser::SetToolbarItems, SetToolbarItems, SetToolbarItems method [Windows Shell], SetToolbarItems method [Windows Shell],IShellBrowser interface, _win32_IShellBrowser_SetToolbarItems, shell.IShellBrowser_SetToolbarItems, shobjidl_core/IShellBrowser::SetToolbarItems
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
 - IShellBrowser::SetToolbarItems
 - shobjidl_core/IShellBrowser::SetToolbarItems
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
 - IShellBrowser.SetToolbarItems
---

# IShellBrowser::SetToolbarItems


## -description

<p class="CCE_Message">[This method has no effect on Windows Vista or later operating systems.]

Adds toolbar items to Windows Explorer's toolbar.

## -parameters

### -param lpButtons

Type: <b>LPTBBUTTONSB</b>

The address of an array of <a href="/windows/desktop/api/commctrl/ns-commctrl-tbbutton">TBBUTTON</a> structures.

### -param nButtons

Type: <b>UINT</b>

The number of <a href="/windows/desktop/api/commctrl/ns-commctrl-tbbutton">TBBUTTON</a> structures in the <i>lpButtons</i> array.

### -param uFlags

Type: <b>UINT</b>

Flags specifying where the toolbar buttons should go. This parameter can be one or more of the following values.



#### FCT_ADDTOEND

Add at the right side of the toolbar.



#### FCT_CONFIGABLE

Not implemented.



#### FCT_MERGE

Merge the toolbar items instead of replacing all of the buttons with those provided by the view. This is the recommended choice.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellbrowser">IShellBrowser</a>