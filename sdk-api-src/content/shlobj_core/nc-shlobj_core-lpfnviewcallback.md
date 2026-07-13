---
UID: NC:shlobj_core.LPFNVIEWCALLBACK
title: LPFNVIEWCALLBACK (shlobj_core.h)
description: Defines the prototype for the callback function used by the system folder view object. This function essentially duplicates the functionality of IShellFolderViewCB.
helpviewer_keywords: ["LPFNVIEWCALLBACK","LPFNVIEWCALLBACK callback","LPFNVIEWCALLBACK callback function [Windows Shell]","SFVM_ADDPROPERTYPAGES","SFVM_BACKGROUNDENUM","SFVM_BACKGROUNDENUMDONE","SFVM_COLUMNCLICK","SFVM_DEFITEMCOUNT","SFVM_DEFVIEWMODE","SFVM_DIDDRAGDROP","SFVM_FSNOTIFY","SFVM_GETANIMATION","SFVM_GETBUTTONINFO","SFVM_GETBUTTONS","SFVM_GETDETAILSOF","SFVM_GETHELPTEXT","SFVM_GETHELPTOPIC","SFVM_GETNOTIFY","SFVM_GETPANE","SFVM_GETSORTDEFAULTS","SFVM_GETTOOLTIPTEXT","SFVM_GETZONE","SFVM_INITMENUPOPUP","SFVM_INVOKECOMMAND","SFVM_MERGEMENU","SFVM_QUERYFSNOTIFY","SFVM_SETISFV","SFVM_SIZE","SFVM_THISIDLIST","SFVM_UNMERGEMENU","SFVM_UPDATESTATUSBAR","SFVM_WINDOWCREATED","_win32_LPFNVIEWCALLBACK","shell.LPFNVIEWCALLBACK","shlobj_core/LPFNVIEWCALLBACK"]
old-location: shell\LPFNVIEWCALLBACK.htm
tech.root: shell
ms.assetid: 744c2b49-017e-4284-a39b-3d317e483316
ms.date: 12/05/2018
ms.keywords: LPFNVIEWCALLBACK, LPFNVIEWCALLBACK callback, LPFNVIEWCALLBACK callback function [Windows Shell], SFVM_ADDPROPERTYPAGES, SFVM_BACKGROUNDENUM, SFVM_BACKGROUNDENUMDONE, SFVM_COLUMNCLICK, SFVM_DEFITEMCOUNT, SFVM_DEFVIEWMODE, SFVM_DIDDRAGDROP, SFVM_FSNOTIFY, SFVM_GETANIMATION, SFVM_GETBUTTONINFO, SFVM_GETBUTTONS, SFVM_GETDETAILSOF, SFVM_GETHELPTEXT, SFVM_GETHELPTOPIC, SFVM_GETNOTIFY, SFVM_GETPANE, SFVM_GETSORTDEFAULTS, SFVM_GETTOOLTIPTEXT, SFVM_GETZONE, SFVM_INITMENUPOPUP, SFVM_INVOKECOMMAND, SFVM_MERGEMENU, SFVM_QUERYFSNOTIFY, SFVM_SETISFV, SFVM_SIZE, SFVM_THISIDLIST, SFVM_UNMERGEMENU, SFVM_UPDATESTATUSBAR, SFVM_WINDOWCREATED, _win32_LPFNVIEWCALLBACK, shell.LPFNVIEWCALLBACK, shlobj_core/LPFNVIEWCALLBACK
req.header: shlobj_core.h
req.include-header: Shlobj.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPFNVIEWCALLBACK
 - shlobj_core/LPFNVIEWCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - shlobj_core.h
api_name:
 - LPFNVIEWCALLBACK
---

# LPFNVIEWCALLBACK callback function


## -description

<p class="CCE_Message">[This interface is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be unsupported in subsequent versions of Windows.]

Defines the prototype for the callback function used by the system folder view object. This function essentially duplicates the functionality of <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb">IShellFolderViewCB</a>.

## -parameters

### -param psvOuter [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>*</b>

A pointer to the owning instance of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a>, if applicable. This parameter can be <b>NULL</b>.

### -param psf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the instance of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> the message applies to.

### -param hwndMain [in]

Type: <b>HWND</b>

The handle of the window that contains the view that receives the message.

### -param uMsg

Type: <b>UINT</b>

One of the following notifications.



#### SFVM_ADDPROPERTYPAGES

Allows the callback object to provide a page to add to the <b>Properties</b> property sheet of the selected object.



#### SFVM_BACKGROUNDENUM

Allows the callback object to request that enumeration be done on a background thread.



#### SFVM_BACKGROUNDENUMDONE

Notifies the callback object that background enumeration is complete.



#### SFVM_COLUMNCLICK

Notifies the callback object that the user has clicked a column header to sort the list of objects in the folder view.



#### SFVM_DEFITEMCOUNT

Allows the callback object to specify the number of items in the folder view.



#### SFVM_DEFVIEWMODE

Allows the callback object to specify the view mode.



#### SFVM_DIDDRAGDROP

Notifies the callback function that a drag-and-drop operation has begun.



#### SFVM_FSNOTIFY

Notifies the callback object that an event has taken place that affects one of its items.



#### SFVM_GETANIMATION

Allows the callback object to specify that an animation be displayed while items are enumerated on a background thread.



#### SFVM_GETBUTTONINFO

Allows the callback object to add buttons to the toolbar.



#### SFVM_GETBUTTONS

Allows the callback object to specify the buttons to be added to the toolbar.



#### SFVM_GETDETAILSOF

Allows the callback object to provide the details for an item in a Shell folder. Use only if a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof">IShellFolder2::GetDetailsOf</a> fails and there is no <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof">IShellDetails::GetDetailsOf</a> method available to call.



#### SFVM_GETHELPTEXT

Allows the callback object to specify a help text string for menu items or toolbar buttons.



#### SFVM_GETHELPTOPIC

Allows the callback object to specify a Help file and topic.



#### SFVM_GETNOTIFY

Specifies which events will generate an <a href="/windows/desktop/shell/sfvm-fsnotify">SFVM_FSNOTIFY</a> message for a given item.



#### SFVM_GETPANE

Allows the callback object to provide the status bar pane in which to display the Internet zone information.



#### SFVM_GETSORTDEFAULTS

Allows the callback object to specify default sorting parameters.



#### SFVM_GETTOOLTIPTEXT

Allows the callback object to specify a <a href="/previous-versions/windows/desktop/legacy/hh449606(v=vs.85)">tooltip</a> text string for menu items or toolbar buttons.



#### SFVM_GETZONE

Allows the callback object to provide Internet zone information.



#### SFVM_INITMENUPOPUP

Allows the callback object to modify an item's context menu.



#### SFVM_INVOKECOMMAND

Notifies the callback object that one of its toolbar or menu commands has been invoked.



#### SFVM_MERGEMENU

Allows the callback object to merge menu items into the Windows Explorer menus.



#### SFVM_QUERYFSNOTIFY

Allows the callback object to register a folder so that changes to that folder's view will generate notifications.



#### SFVM_SETISFV

Notifies the callback object of the container site. This is used only when <a href="/windows/desktop/api/ocidl/nf-ocidl-iobjectwithsite-setsite">IObjectWithSite::SetSite</a> is not supported and <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex">SHCreateShellFolderViewEx</a> is used.



#### SFVM_SIZE

Notifies the callback object that the folder view has been resized.



#### SFVM_THISIDLIST

Allows the callback object to specify the view's PIDL. This is used only when <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist">IPersistIDList::SetIDList</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder">IPersistFolder2::GetCurFolder</a> have failed.



#### SFVM_UNMERGEMENU

Notifies the callback object that a menu is being removed.



#### SFVM_UPDATESTATUSBAR

Allows the callback object to request that the status bar be updated.



#### SFVM_WINDOWCREATED

Notifies the callback object that the folder view window is being created.

### -param wParam

Type: <b>WPARAM</b>

Additional information dependent on the value in <i>uMsg</i>. See the individual notification pages for specific requirements.

### -param lParam

Type: <b>LPARAM</b>

Additional information dependent on the value in <i>uMsg</i>. See the individual notification pages for specific requirements.

## -returns

Type: <b>HRESULT</b>

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-ishellfolderviewcb">IShellFolderViewCB</a>
