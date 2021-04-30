---
UID: NF:commctrl.ShowHideMenuCtl
title: ShowHideMenuCtl function (commctrl.h)
description: Sets or removes the specified menu item's check mark attribute and shows or hides the corresponding control.
helpviewer_keywords: ["ShowHideMenuCtl","ShowHideMenuCtl function [Windows Controls]","_win32_ShowHideMenuCtl","_win32_ShowHideMenuCtl_cpp","commctrl/ShowHideMenuCtl","controls.ShowHideMenuCtl","controls._win32_ShowHideMenuCtl"]
old-location: controls\ShowHideMenuCtl.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\showhidemenuctl.htm
ms.date: 12/05/2018
ms.keywords: ShowHideMenuCtl, ShowHideMenuCtl function [Windows Controls], _win32_ShowHideMenuCtl, _win32_ShowHideMenuCtl_cpp, commctrl/ShowHideMenuCtl, controls.ShowHideMenuCtl, controls._win32_ShowHideMenuCtl
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ShowHideMenuCtl
 - commctrl/ShowHideMenuCtl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ShowHideMenuCtl
---

# ShowHideMenuCtl function


## -description

<p class="CCE_Message">[<b>ShowHideMenuCtl</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Sets or removes the specified menu item's check mark attribute and shows or hides the corresponding control. The function adds a check mark to the specified menu item if it does not have one and then displays the corresponding control. If the menu item already has a check mark, the function removes the check mark and hides the corresponding control.

## -parameters

### -param hWnd

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the window that contains the menu and controls.

### -param uFlags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT_PTR</a></b>

The identifier of the menu item to receive or lose a check mark.

### -param lpInfo

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPINT</a></b>

A pointer to an array that contains pairs of values. The second value in the first pair must be the handle to the application's main menu. Each subsequent pair consists of a menu item identifier and a control window identifier. The function searches the array for a value that matches <i>uFlags</i> and, if the value is found, checks or unchecks the menu item and shows or hides the corresponding control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.