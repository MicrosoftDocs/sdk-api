---
UID: NF:dwmapi.DwmGetUnmetTabRequirements
title: DwmGetUnmetTabRequirements function
author: windows-sdk-content
description: Note  This function is publically available, but nonfunctional, for Windows 10, version 1803.Checks the requirements needed to get tabs in the application title bar for the specified window.
old-location: dwm\dwmgetunmettabrequirements.htm
old-project: dwm
ms.assetid: 8E67E1BE-D6FC-4A8A-8E71-45B6F337E3BD
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DwmGetUnmetTabRequirements, DwmGetUnmetTabRequirements function [Desktop Window Manager], dwm.dwmgetunmettabrequirements, dwmapi/DwmGetUnmetTabRequirements
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dwmapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dwmapi.dll
api_name:
 - DwmGetUnmetTabRequirements
product: Windows
targetos: Windows
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DwmGetUnmetTabRequirements function


## -description



<b>Note</b>  This function is publically available, but nonfunctional, for Windows 10, version 1803.</p>Checks the requirements needed to get tabs in the application title bar for the specified window.


## -parameters




### -param appWindow [in, optional]

The handle of the window to check.


### -param param

TBD




#### - value [out]

On success, returns a pointer to a   <a href="https://msdn.microsoft.com/8366ABE4-263D-448D-9FC9-3F4DAF9B700D">DWM_TAB_WINDOW_REQUIREMENTS</a> value describing the requirements for placing a tab.

If <b>DWMTWR_NONE</b>, the window is capable of
receiving tabs in its title bar.  Otherwise, indicates the reason why the application is ineligible.


