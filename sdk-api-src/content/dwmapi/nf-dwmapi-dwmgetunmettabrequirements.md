---
UID: NF:dwmapi.DwmGetUnmetTabRequirements
title: DwmGetUnmetTabRequirements function (dwmapi.h)
description: Note  This function is publically available, but nonfunctional, for Windows 10, version 1803.Checks the requirements needed to get tabs in the application title bar for the specified window.
helpviewer_keywords: ["DwmGetUnmetTabRequirements","DwmGetUnmetTabRequirements function [Desktop Window Manager]","dwm.dwmgetunmettabrequirements","dwmapi/DwmGetUnmetTabRequirements"]
old-location: dwm\dwmgetunmettabrequirements.htm
tech.root: dwm
ms.assetid: 8E67E1BE-D6FC-4A8A-8E71-45B6F337E3BD
ms.date: 12/05/2018
ms.keywords: DwmGetUnmetTabRequirements, DwmGetUnmetTabRequirements function [Desktop Window Manager], dwm.dwmgetunmettabrequirements, dwmapi/DwmGetUnmetTabRequirements
req.header: dwmapi.h
req.include-header: 
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
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmGetUnmetTabRequirements
 - dwmapi/DwmGetUnmetTabRequirements
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dwmapi.dll
api_name:
 - DwmGetUnmetTabRequirements
---

# DwmGetUnmetTabRequirements function


## -description

<b>Note</b>  This function is publically available, but nonfunctional, for Windows 10, version 1803.</p>Checks the requirements needed to get tabs in the application title bar for the specified window.

## -parameters

### -param appWindow [in, optional]

The handle of the window to check.

### -param unnamedParam2 [out]

On success, returns a pointer to a   <a href="/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements">DWM_TAB_WINDOW_REQUIREMENTS</a> value describing the requirements for placing a tab.

If <b>DWMTWR_NONE</b>, the window is capable of
receiving tabs in its title bar.  Otherwise, indicates the reason why the application is ineligible.