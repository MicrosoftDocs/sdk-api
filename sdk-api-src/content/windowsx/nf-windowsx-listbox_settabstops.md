---
UID: NF:windowsx.ListBox_SetTabStops
title: ListBox_SetTabStops macro
author: windows-sdk-content
description: Sets the tab-stop positions in a list box. You can use this macro or send the LB_SETTABSTOPS message explicitly.
old-location: controls\ListBox_SetTabStops.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxmacros\listbox_settabstops.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListBox_SetTabStops, ListBox_SetTabStops macro [Windows Controls], _win32_ListBox_SetTabStops, _win32_ListBox_SetTabStops_cpp, controls.ListBox_SetTabStops, controls._win32_ListBox_SetTabStops, windowsx/ListBox_SetTabStops
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: windowsx.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Windowsx.h
api_name:
 - ListBox_SetTabStops
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListBox_SetTabStops macro


## -description


Sets the tab-stop positions in a list box. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761354(v=VS.85).aspx">LB_SETTABSTOPS</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param cTabs

Type: <b>int</b>

The number of elements in the <i>lpTabs</i> array.


### -param lpTabs

Type: <b>int*</b>

A pointer to an array of integers containing the tab stops. The integers represent the number of quarters of the average character width for the font that is selected into the list box. For example, a tab stop of 4 is placed at 1.0 character units, and a tab stop of 6 is placed at 1.5 average character units. However, if the list box is part of a dialog box, the integers are in dialog template units. The tab stops must be sorted in ascending order; backward tabs are not allowed.


## -remarks



For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb761354(v=VS.85).aspx">LB_SETTABSTOPS</a>.
	



