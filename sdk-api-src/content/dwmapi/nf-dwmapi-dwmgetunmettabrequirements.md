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

# DwmGetUnmetTabRequirements function


## -description



<b>Note</b>  This function is publically available, but nonfunctional, for Windows 10, version 1803.</p>Checks the requirements needed to get tabs in the application title bar for the specified window.


## -parameters




### -param appWindow [in, optional]

The handle of the window to check.


### -param value [out]

On success, returns a pointer to a   <a href="https://msdn.microsoft.com/8366ABE4-263D-448D-9FC9-3F4DAF9B700D">DWM_TAB_WINDOW_REQUIREMENTS</a> value describing the requirements for placing a tab.

If <b>DWMTWR_NONE</b>, the window is capable of
receiving tabs in its title bar.  Otherwise, indicates the reason why the application is ineligible.


