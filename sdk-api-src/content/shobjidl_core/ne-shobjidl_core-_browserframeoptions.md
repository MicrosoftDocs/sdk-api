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

# _BROWSERFRAMEOPTIONS enumeration


## -description


Used with method <a href="https://msdn.microsoft.com/4f0e9f69-92e5-4fec-bdfa-b37d594ff5fe">IBrowserFrameOptions::GetFrameOptions</a>.


## -enum-fields




### -field BFO_NONE

Do nothing.


### -field BFO_BROWSER_PERSIST_SETTINGS

Use the browser stream for this item. (Same window position as IE browser windows.)


### -field BFO_RENAME_FOLDER_OPTIONS_TOINTERNET

Rename <b>Folder Options</b> to <b>Internet Options</b> in the Tools or View menu.


### -field BFO_BOTH_OPTIONS

Keep both <b>Folder Options</b> and <b>Internet Options</b> in the Tools or View menu.


### -field BIF_PREFER_INTERNET_SHORTCUT

This namespace extension prefers a .url shortcut over a .lnk shortcut.


### -field BFO_BROWSE_NO_IN_NEW_PROCESS

Do not use "Browse in New Process" by invoking a shortcut.


### -field BFO_ENABLE_HYPERLINK_TRACKING

Track display name to determine when hyperlinks should be tagged as previously used.


### -field BFO_USE_IE_OFFLINE_SUPPORT

Use Internet Explorer's offline support.


### -field BFO_SUBSTITUE_INTERNET_START_PAGE

Use Start Page support for this namespace extension.


### -field BFO_USE_IE_LOGOBANDING

Use the Brand block in the Toolbar.


### -field BFO_ADD_IE_TOCAPTIONBAR

Append <code>" - Internet Explorer"</code> to display name in the caption bar.


### -field BFO_USE_DIALUP_REF

Reference the DialUp reference count while the browser is navigated to this location. This will also enable the ICW and Software update.


### -field BFO_USE_IE_TOOLBAR

Use the Internet Explorer toolbar.


### -field BFO_NO_PARENT_FOLDER_SUPPORT

Disable navigation to parent folders. Used for the button that navigates to parent folder or the View.GoTo.ParentFolder feature.


### -field BFO_NO_REOPEN_NEXT_RESTART

Browser windows are not reopened after a reboot of the system, regardless of whether they were open before the reboot. Use the same behavior for the namespace extension.


### -field BFO_GO_HOME_PAGE

Add <b>Home Page</b> to menu (Go).


### -field BFO_PREFER_IEPROCESS

Prefer use of Iexplore.exe over Explorer.exe.


### -field BFO_SHOW_NAVIGATION_CANCELLED

If navigation is terminated, show the <b>Action Canceled</b> HTML page.


### -field BFO_USE_IE_STATUSBAR

Use the persisted Internet Explorer status bar settings.


### -field BFO_QUERY_ALL

Return all values.


## -remarks



These constants are defined in the Shobjidl.h file beginning in Windows Vista.



