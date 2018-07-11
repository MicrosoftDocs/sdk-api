---
UID: NE:shobjidl_core.EXPLORER_BROWSER_OPTIONS
title: EXPLORER_BROWSER_OPTIONS
author: windows-sdk-content
description: These flags are used with IExplorerBrowser::GetOptions and IExplorerBrowser::SetOptions.
old-location: shell\EXPLORER_BROWSER_OPTIONS.htm
old-project: shell
ms.assetid: 4e2983bc-cad2-4bcc-8169-57b5274b2142
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: EBO_ALWAYSNAVIGATE, EBO_HTMLSHAREPOINTVIEW, EBO_NAVIGATEONCE, EBO_NOBORDER, EBO_NONE, EBO_NOPERSISTVIEWSTATE, EBO_NOTRAVELLOG, EBO_NOWRAPPERWINDOW, EBO_SHOWFRAMES, EXPLORER_BROWSER_OPTIONS, EXPLORER_BROWSER_OPTIONS enumeration [Windows Shell], _shell_EXPLORER_BROWSER_OPTIONS, shell.EXPLORER_BROWSER_OPTIONS, shobjidl_core/EBO_ALWAYSNAVIGATE, shobjidl_core/EBO_HTMLSHAREPOINTVIEW, shobjidl_core/EBO_NAVIGATEONCE, shobjidl_core/EBO_NOBORDER, shobjidl_core/EBO_NONE, shobjidl_core/EBO_NOPERSISTVIEWSTATE, shobjidl_core/EBO_NOTRAVELLOG, shobjidl_core/EBO_NOWRAPPERWINDOW, shobjidl_core/EBO_SHOWFRAMES, shobjidl_core/EXPLORER_BROWSER_OPTIONS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: EXPLORER_BROWSER_OPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - EXPLORER_BROWSER_OPTIONS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# EXPLORER_BROWSER_OPTIONS enumeration


## -description


These flags are used with <a href="https://msdn.microsoft.com/e2c7ee6a-fbd9-4b75-a9ed-734e7977088d">IExplorerBrowser::GetOptions</a> and <a href="https://msdn.microsoft.com/b2f8fe1b-afcd-4fb0-b96b-41e38c7fea0b">IExplorerBrowser::SetOptions</a>.


## -enum-fields




### -field EBO_NONE

No options.


### -field EBO_NAVIGATEONCE

Do not navigate further than the initial navigation.


### -field EBO_SHOWFRAMES

Use the following standard panes: Commands Module pane, Navigation pane, Details pane, and Preview pane. An implementer of <a href="https://msdn.microsoft.com/b940adc2-dfef-49c5-b86c-d0da83db0aad">IExplorerPaneVisibility</a> can modify the components of the Commands Module that  are shown. For more information see, <a href="https://msdn.microsoft.com/6c051cdc-b7f9-48dc-ba32-38f0f1ee5fda">IExplorerPaneVisibility::GetPaneState</a>. If EBO_SHOWFRAMES is not set, Explorer browser uses a single view object.


### -field EBO_ALWAYSNAVIGATE

Always navigate, even if you are attempting to navigate to the current folder.


### -field EBO_NOTRAVELLOG

Do not update the travel log.


### -field EBO_NOWRAPPERWINDOW

Do not use a wrapper window. This flag is used with legacy clients that need the browser parented directly on themselves.


### -field EBO_HTMLSHAREPOINTVIEW

Show WebView for sharepoint sites.


### -field EBO_NOBORDER

<b>Introduced in Windows Vista</b>. Do not draw a border around the browser window.


### -field EBO_NOPERSISTVIEWSTATE

<b>Introduced in Windows Vista</b>. Do not persist the view state.

