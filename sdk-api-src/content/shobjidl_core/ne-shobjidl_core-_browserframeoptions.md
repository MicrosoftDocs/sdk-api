---
UID: NE:shobjidl_core._BROWSERFRAMEOPTIONS
title: _BROWSERFRAMEOPTIONS (shobjidl_core.h)
description: Used with method IBrowserFrameOptions::GetFrameOptions.
helpviewer_keywords: ["BFO_ADD_IE_TOCAPTIONBAR","BFO_BOTH_OPTIONS","BFO_BROWSER_PERSIST_SETTINGS","BFO_BROWSE_NO_IN_NEW_PROCESS","BFO_ENABLE_HYPERLINK_TRACKING","BFO_GO_HOME_PAGE","BFO_NONE","BFO_NO_PARENT_FOLDER_SUPPORT","BFO_NO_REOPEN_NEXT_RESTART","BFO_PREFER_IEPROCESS","BFO_QUERY_ALL","BFO_RENAME_FOLDER_OPTIONS_TOINTERNET","BFO_SHOW_NAVIGATION_CANCELLED","BFO_SUBSTITUE_INTERNET_START_PAGE","BFO_USE_DIALUP_REF","BFO_USE_IE_LOGOBANDING","BFO_USE_IE_OFFLINE_SUPPORT","BFO_USE_IE_STATUSBAR","BFO_USE_IE_TOOLBAR","BIF_PREFER_INTERNET_SHORTCUT","BROWSERFRAMEOPTIONS","BROWSERFRAMEOPTIONS enumeration [Windows Shell]","_BROWSERFRAMEOPTIONS","_shell_BROWSERFRAMEOPTIONS","shell.BROWSERFRAMEOPTIONS","shobjidl_core/BFO_ADD_IE_TOCAPTIONBAR","shobjidl_core/BFO_BOTH_OPTIONS","shobjidl_core/BFO_BROWSER_PERSIST_SETTINGS","shobjidl_core/BFO_BROWSE_NO_IN_NEW_PROCESS","shobjidl_core/BFO_ENABLE_HYPERLINK_TRACKING","shobjidl_core/BFO_GO_HOME_PAGE","shobjidl_core/BFO_NONE","shobjidl_core/BFO_NO_PARENT_FOLDER_SUPPORT","shobjidl_core/BFO_NO_REOPEN_NEXT_RESTART","shobjidl_core/BFO_PREFER_IEPROCESS","shobjidl_core/BFO_QUERY_ALL","shobjidl_core/BFO_RENAME_FOLDER_OPTIONS_TOINTERNET","shobjidl_core/BFO_SHOW_NAVIGATION_CANCELLED","shobjidl_core/BFO_SUBSTITUE_INTERNET_START_PAGE","shobjidl_core/BFO_USE_DIALUP_REF","shobjidl_core/BFO_USE_IE_LOGOBANDING","shobjidl_core/BFO_USE_IE_OFFLINE_SUPPORT","shobjidl_core/BFO_USE_IE_STATUSBAR","shobjidl_core/BFO_USE_IE_TOOLBAR","shobjidl_core/BIF_PREFER_INTERNET_SHORTCUT","shobjidl_core/BROWSERFRAMEOPTIONS"]
old-location: shell\BROWSERFRAMEOPTIONS.htm
tech.root: shell
ms.assetid: e1c75a00-304f-44ca-98a0-a6c76a1ef95f
ms.date: 12/05/2018
ms.keywords: BFO_ADD_IE_TOCAPTIONBAR, BFO_BOTH_OPTIONS, BFO_BROWSER_PERSIST_SETTINGS, BFO_BROWSE_NO_IN_NEW_PROCESS, BFO_ENABLE_HYPERLINK_TRACKING, BFO_GO_HOME_PAGE, BFO_NONE, BFO_NO_PARENT_FOLDER_SUPPORT, BFO_NO_REOPEN_NEXT_RESTART, BFO_PREFER_IEPROCESS, BFO_QUERY_ALL, BFO_RENAME_FOLDER_OPTIONS_TOINTERNET, BFO_SHOW_NAVIGATION_CANCELLED, BFO_SUBSTITUE_INTERNET_START_PAGE, BFO_USE_DIALUP_REF, BFO_USE_IE_LOGOBANDING, BFO_USE_IE_OFFLINE_SUPPORT, BFO_USE_IE_STATUSBAR, BFO_USE_IE_TOOLBAR, BIF_PREFER_INTERNET_SHORTCUT, BROWSERFRAMEOPTIONS, BROWSERFRAMEOPTIONS enumeration [Windows Shell], _BROWSERFRAMEOPTIONS, _shell_BROWSERFRAMEOPTIONS, shell.BROWSERFRAMEOPTIONS, shobjidl_core/BFO_ADD_IE_TOCAPTIONBAR, shobjidl_core/BFO_BOTH_OPTIONS, shobjidl_core/BFO_BROWSER_PERSIST_SETTINGS, shobjidl_core/BFO_BROWSE_NO_IN_NEW_PROCESS, shobjidl_core/BFO_ENABLE_HYPERLINK_TRACKING, shobjidl_core/BFO_GO_HOME_PAGE, shobjidl_core/BFO_NONE, shobjidl_core/BFO_NO_PARENT_FOLDER_SUPPORT, shobjidl_core/BFO_NO_REOPEN_NEXT_RESTART, shobjidl_core/BFO_PREFER_IEPROCESS, shobjidl_core/BFO_QUERY_ALL, shobjidl_core/BFO_RENAME_FOLDER_OPTIONS_TOINTERNET, shobjidl_core/BFO_SHOW_NAVIGATION_CANCELLED, shobjidl_core/BFO_SUBSTITUE_INTERNET_START_PAGE, shobjidl_core/BFO_USE_DIALUP_REF, shobjidl_core/BFO_USE_IE_LOGOBANDING, shobjidl_core/BFO_USE_IE_OFFLINE_SUPPORT, shobjidl_core/BFO_USE_IE_STATUSBAR, shobjidl_core/BFO_USE_IE_TOOLBAR, shobjidl_core/BIF_PREFER_INTERNET_SHORTCUT, shobjidl_core/BROWSERFRAMEOPTIONS
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _BROWSERFRAMEOPTIONS
 - shobjidl_core/_BROWSERFRAMEOPTIONS
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
 - BROWSERFRAMEOPTIONS
---

# _BROWSERFRAMEOPTIONS enumeration


## -description

Used with method <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ibrowserframeoptions-getframeoptions">IBrowserFrameOptions::GetFrameOptions</a>.

## -enum-fields

### -field BFO_NONE:0

Do nothing.

### -field BFO_BROWSER_PERSIST_SETTINGS:0x1

Use the browser stream for this item. (Same window position as IE browser windows.)

### -field BFO_RENAME_FOLDER_OPTIONS_TOINTERNET:0x2

Rename <b>Folder Options</b> to <b>Internet Options</b> in the Tools or View menu.

### -field BFO_BOTH_OPTIONS:0x4

Keep both <b>Folder Options</b> and <b>Internet Options</b> in the Tools or View menu.

### -field BIF_PREFER_INTERNET_SHORTCUT:0x8

This namespace extension prefers a .url shortcut over a .lnk shortcut.

### -field BFO_BROWSE_NO_IN_NEW_PROCESS:0x10

Do not use "Browse in New Process" by invoking a shortcut.

### -field BFO_ENABLE_HYPERLINK_TRACKING:0x20

Track display name to determine when hyperlinks should be tagged as previously used.

### -field BFO_USE_IE_OFFLINE_SUPPORT:0x40

Use Internet Explorer's offline support.

### -field BFO_SUBSTITUE_INTERNET_START_PAGE:0x80

Use Start Page support for this namespace extension.

### -field BFO_USE_IE_LOGOBANDING:0x100

Use the Brand block in the Toolbar.

### -field BFO_ADD_IE_TOCAPTIONBAR:0x200

Append <code>" - Internet Explorer"</code> to display name in the caption bar.

### -field BFO_USE_DIALUP_REF:0x400

Reference the DialUp reference count while the browser is navigated to this location. This will also enable the ICW and Software update.

### -field BFO_USE_IE_TOOLBAR:0x800

Use the Internet Explorer toolbar.

### -field BFO_NO_PARENT_FOLDER_SUPPORT:0x1000

Disable navigation to parent folders. Used for the button that navigates to parent folder or the View.GoTo.ParentFolder feature.

### -field BFO_NO_REOPEN_NEXT_RESTART:0x2000

Browser windows are not reopened after a reboot of the system, regardless of whether they were open before the reboot. Use the same behavior for the namespace extension.

### -field BFO_GO_HOME_PAGE:0x4000

Add <b>Home Page</b> to menu (Go).

### -field BFO_PREFER_IEPROCESS:0x8000

Prefer use of Iexplore.exe over Explorer.exe.

### -field BFO_SHOW_NAVIGATION_CANCELLED:0x10000

If navigation is terminated, show the <b>Action Canceled</b> HTML page.

### -field BFO_USE_IE_STATUSBAR:0x20000

Use the persisted Internet Explorer status bar settings.

### -field BFO_QUERY_ALL

Return all values.

## -remarks

These constants are defined in the Shobjidl.h file beginning in Windows Vista.
