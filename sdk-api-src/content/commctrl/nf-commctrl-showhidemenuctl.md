---
UID: NF:commctrl.ShowHideMenuCtl
title: ShowHideMenuCtl function
author: windows-sdk-content
description: Sets or removes the specified menu item's check mark attribute and shows or hides the corresponding control.
old-location: controls\ShowHideMenuCtl.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\common\functions\showhidemenuctl.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: ShowHideMenuCtl, ShowHideMenuCtl function [Windows Controls], _win32_ShowHideMenuCtl, _win32_ShowHideMenuCtl_cpp, commctrl/ShowHideMenuCtl, controls.ShowHideMenuCtl, controls._win32_ShowHideMenuCtl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - ShowHideMenuCtl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ShowHideMenuCtl function


## -description


<p class="CCE_Message">[<b>ShowHideMenuCtl</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Sets or removes the specified menu item's check mark attribute and shows or hides the corresponding control. The function adds a check mark to the specified menu item if it does not have one and then displays the corresponding control. If the menu item already has a check mark, the function removes the check mark and hides the corresponding control. 


## -parameters




### -param hWnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the window that contains the menu and controls. 


### -param uFlags

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">UINT_PTR</a></b>

The identifier of the menu item to receive or lose a check mark. 


### -param lpInfo

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPINT</a></b>

A pointer to an array that contains pairs of values. The second value in the first pair must be the handle to the application's main menu. Each subsequent pair consists of a menu item identifier and a control window identifier. The function searches the array for a value that matches <i>uFlags</i> and, if the value is found, checks or unchecks the menu item and shows or hides the corresponding control. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 



