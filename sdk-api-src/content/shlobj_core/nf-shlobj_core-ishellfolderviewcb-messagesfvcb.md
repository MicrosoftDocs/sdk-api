---
UID: NF:shlobj_core.IShellFolderViewCB.MessageSFVCB
title: IShellFolderViewCB::MessageSFVCB (shlobj_core.h)
description: Allows communication between the system folder view object and a system folder view callback object.
helpviewer_keywords: ["IShellFolderViewCB interface [Windows Shell]","MessageSFVCB method","IShellFolderViewCB.MessageSFVCB","IShellFolderViewCB::MessageSFVCB","MessageSFVCB","MessageSFVCB method [Windows Shell]","MessageSFVCB method [Windows Shell]","IShellFolderViewCB interface","_win32_IShellFolderViewCB_MessageSFVCB","shell.IShellFolderViewCB_MessageSFVCB","shlobj_core/IShellFolderViewCB::MessageSFVCB"]
old-location: shell\IShellFolderViewCB_MessageSFVCB.htm
tech.root: shell
ms.assetid: 1678dd76-6ed4-4625-9170-22dcd3d7e8d2
ms.date: 12/05/2018
ms.keywords: IShellFolderViewCB interface [Windows Shell],MessageSFVCB method, IShellFolderViewCB.MessageSFVCB, IShellFolderViewCB::MessageSFVCB, MessageSFVCB, MessageSFVCB method [Windows Shell], MessageSFVCB method [Windows Shell],IShellFolderViewCB interface, _win32_IShellFolderViewCB_MessageSFVCB, shell.IShellFolderViewCB_MessageSFVCB, shlobj_core/IShellFolderViewCB::MessageSFVCB
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolderViewCB::MessageSFVCB
 - shlobj_core/IShellFolderViewCB::MessageSFVCB
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
 - IShellFolderViewCB.MessageSFVCB
---

# IShellFolderViewCB::MessageSFVCB


## -description

Allows communication between the system folder view object and a system folder view callback object.

## -parameters

### -param uMsg [in]

Type: <b>UINT</b>

One of the following notifications.
					
				

<table class="clsStd">
<tr>
<th>Notification</th>
<th>Usage</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-addpropertypages">SFVM_ADDPROPERTYPAGES</a>
</td>
<td>Allows the callback object to provide a page to add to the <b>Properties</b> property sheet of the selected object.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-backgroundenum">SFVM_BACKGROUNDENUM</a>
</td>
<td>Allows the callback object to request that enumeration be done on a background thread.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-backgroundenumdone">SFVM_BACKGROUNDENUMDONE</a>
</td>
<td>Notifies the callback object that background enumeration is complete.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-columnclick">SFVM_COLUMNCLICK</a>
</td>
<td>Notifies the callback object that the user has clicked a column header to sort the list of objects in the folder view.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-defitemcount">SFVM_DEFITEMCOUNT</a>
</td>
<td>Allows the callback object to specify the number of items in the folder view.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-defviewmode">SFVM_DEFVIEWMODE</a>
</td>
<td>Allows the callback object to specify the view mode.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-diddragdrop">SFVM_DIDDRAGDROP</a>
</td>
<td>Notifies the callback function that a drag-and-drop operation has begun.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-fsnotify">SFVM_FSNOTIFY</a>
</td>
<td>Notifies the callback object that an event has taken place that affects one of its items.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-getanimation">SFVM_GETANIMATION</a>
</td>
<td>Allows the callback object to specify that an animation be displayed while items are enumerated on a background thread.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-getbuttoninfo">SFVM_GETBUTTONINFO</a>
</td>
<td>Allows the callback object to add buttons to the toolbar.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-getbuttons">SFVM_GETBUTTONS</a>
</td>
<td>Allows the callback object to specify the buttons to be added to the toolbar.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-getdetailsof">SFVM_GETDETAILSOF</a>
</td>
<td>Allows the callback object to provide the details for an item in a Shell folder. Use only if a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof">GetDetailsOf</a> fails and there is no <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof">GetDetailsOf</a> method available to call.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-gethelptext">SFVM_GETHELPTEXT</a>
</td>
<td>Allows the callback object to specify a help text string for menu items or toolbar buttons.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-gethelptopic">SFVM_GETHELPTOPIC</a>
</td>
<td>Allows the callback object to specify a Help file and topic.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-getnotify">SFVM_GETNOTIFY</a>
</td>
<td>Specifies which events will generate an <a href="/windows/desktop/shell/sfvm-fsnotify">SFVM_FSNOTIFY</a> message for a given item.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-getpane">SFVM_GETPANE</a>
</td>
<td>Allows the callback object to provide the status bar pane in which to display the Internet zone information.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-getsortdefaults">SFVM_GETSORTDEFAULTS</a>
</td>
<td>Allows the callback object to specify default sorting parameters.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-gettooltiptext">SFVM_GETTOOLTIPTEXT</a>
</td>
<td>Allows the callback object to specify a <a href="/windows/desktop/Controls/tooltip-controls">tooltip</a> text string for menu items or toolbar buttons.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-getzone">SFVM_GETZONE</a>
</td>
<td>Allows the callback object to provide Internet zone information.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-initmenupopup">SFVM_INITMENUPOPUP</a>
</td>
<td>Allows the callback object to modify an item's context menu.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-invokecommand">SFVM_INVOKECOMMAND</a>
</td>
<td>Notifies the callback object that one of its toolbar or menu commands has been invoked.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-mergemenu">SFVM_MERGEMENU</a>
</td>
<td>Allows the callback object to merge menu items into the Windows Explorer menus.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-queryfsnotify">SFVM_QUERYFSNOTIFY</a>
</td>
<td>Allows the callback object to register a folder so that changes to that folder's view will generate notifications.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-setisfv">SFVM_SETISFV</a>
</td>
<td>Notifies the callback object of the container site. This is used only when <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">IObjectWithSite::SetSite</a> is not supported and <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a> is used.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-size">SFVM_SIZE</a>
</td>
<td>Notifies the callback object that the folder view has been resized.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-thisidlist">SFVM_THISIDLIST</a>
</td>
<td>Allows the callback object to specify the view's PIDL. This is used only when <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist">SetIDList</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder">IPersistFolder2::GetCurFolder</a> have failed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-unmergemenu">SFVM_UNMERGEMENU</a>
</td>
<td>Notifies the callback object that a menu is being removed.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-updatestatusbar">SFVM_UPDATESTATUSBAR</a>
</td>
<td>Allows the callback object to request that the status bar be updated.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/sfvm-windowcreated">SFVM_WINDOWCREATED</a>
</td>
<td>Notifies the callback object that the folder view window is being created.</td>
</tr>
</table>

### -param wParam

Type: <b>WPARAM</b>

Additional information. See the individual notification pages for specific requirements.

### -param lParam

Type: <b>LPARAM</b>

Additional information. See the individual notification pages for specific requirements.

## -returns

Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The notification has been handled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The message has not been handled and the system folder view object should perform default processing.

</td>
</tr>
</table>