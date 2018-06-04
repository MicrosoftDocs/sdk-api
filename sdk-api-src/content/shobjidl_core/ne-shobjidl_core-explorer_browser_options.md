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

