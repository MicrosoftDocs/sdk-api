---
UID: NE:shobjidl_core.EXPLORER_BROWSER_OPTIONS
title: EXPLORER_BROWSER_OPTIONS (shobjidl_core.h)
description: These flags are used with IExplorerBrowser::GetOptions and IExplorerBrowser::SetOptions.
helpviewer_keywords: ["EBO_ALWAYSNAVIGATE","EBO_HTMLSHAREPOINTVIEW","EBO_NAVIGATEONCE","EBO_NOBORDER","EBO_NONE","EBO_NOPERSISTVIEWSTATE","EBO_NOTRAVELLOG","EBO_NOWRAPPERWINDOW","EBO_SHOWFRAMES","EXPLORER_BROWSER_OPTIONS","EXPLORER_BROWSER_OPTIONS enumeration [Windows Shell]","_shell_EXPLORER_BROWSER_OPTIONS","shell.EXPLORER_BROWSER_OPTIONS","shobjidl_core/EBO_ALWAYSNAVIGATE","shobjidl_core/EBO_HTMLSHAREPOINTVIEW","shobjidl_core/EBO_NAVIGATEONCE","shobjidl_core/EBO_NOBORDER","shobjidl_core/EBO_NONE","shobjidl_core/EBO_NOPERSISTVIEWSTATE","shobjidl_core/EBO_NOTRAVELLOG","shobjidl_core/EBO_NOWRAPPERWINDOW","shobjidl_core/EBO_SHOWFRAMES","shobjidl_core/EXPLORER_BROWSER_OPTIONS"]
old-location: shell\EXPLORER_BROWSER_OPTIONS.htm
tech.root: shell
ms.assetid: 4e2983bc-cad2-4bcc-8169-57b5274b2142
ms.date: 12/05/2018
ms.keywords: EBO_ALWAYSNAVIGATE, EBO_HTMLSHAREPOINTVIEW, EBO_NAVIGATEONCE, EBO_NOBORDER, EBO_NONE, EBO_NOPERSISTVIEWSTATE, EBO_NOTRAVELLOG, EBO_NOWRAPPERWINDOW, EBO_SHOWFRAMES, EXPLORER_BROWSER_OPTIONS, EXPLORER_BROWSER_OPTIONS enumeration [Windows Shell], _shell_EXPLORER_BROWSER_OPTIONS, shell.EXPLORER_BROWSER_OPTIONS, shobjidl_core/EBO_ALWAYSNAVIGATE, shobjidl_core/EBO_HTMLSHAREPOINTVIEW, shobjidl_core/EBO_NAVIGATEONCE, shobjidl_core/EBO_NOBORDER, shobjidl_core/EBO_NONE, shobjidl_core/EBO_NOPERSISTVIEWSTATE, shobjidl_core/EBO_NOTRAVELLOG, shobjidl_core/EBO_NOWRAPPERWINDOW, shobjidl_core/EBO_SHOWFRAMES, shobjidl_core/EXPLORER_BROWSER_OPTIONS
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EXPLORER_BROWSER_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EXPLORER_BROWSER_OPTIONS
 - shobjidl_core/EXPLORER_BROWSER_OPTIONS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - EXPLORER_BROWSER_OPTIONS
---

# EXPLORER_BROWSER_OPTIONS enumeration


## -description

These flags are used with <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-getoptions">IExplorerBrowser::GetOptions</a> and <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerbrowser-setoptions">IExplorerBrowser::SetOptions</a>.

## -enum-fields

### -field EBO_NONE:0

No options.

### -field EBO_NAVIGATEONCE:0x1

Do not navigate further than the initial navigation.

### -field EBO_SHOWFRAMES:0x2

Use the following standard panes: Commands Module pane, Navigation pane, Details pane, and Preview pane. An implementer of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorerpanevisibility">IExplorerPaneVisibility</a> can modify the components of the Commands Module that  are shown. For more information see, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate">IExplorerPaneVisibility::GetPaneState</a>. If EBO_SHOWFRAMES is not set, Explorer browser uses a single view object.

### -field EBO_ALWAYSNAVIGATE:0x4

Always navigate, even if you are attempting to navigate to the current folder.

### -field EBO_NOTRAVELLOG:0x8

Do not update the travel log.

### -field EBO_NOWRAPPERWINDOW:0x10

Do not use a wrapper window. This flag is used with legacy clients that need the browser parented directly on themselves.

### -field EBO_HTMLSHAREPOINTVIEW:0x20

Show WebView for sharepoint sites.

### -field EBO_NOBORDER:0x40

<b>Introduced in Windows Vista</b>. Do not draw a border around the browser window.

### -field EBO_NOPERSISTVIEWSTATE:0x80

<b>Introduced in Windows Vista</b>. Do not persist the view state.
