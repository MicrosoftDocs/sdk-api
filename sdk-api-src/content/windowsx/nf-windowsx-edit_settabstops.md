---
UID: NF:windowsx.Edit_SetTabStops
title: Edit_SetTabStops macro
author: windows-sdk-content
description: Sets the tab stops in a multiline edit or rich edit control. When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop. You can use this macro or send the EM_SETTABSTOPS message explicitly.
old-location: controls\Edit_SetTabStops.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\editcontrols\editcontrolreference\editcontrolmacros\edit_settabstops.htm
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: Edit_SetTabStops, Edit_SetTabStops macro [Windows Controls], _win32_Edit_SetTabStops, _win32_Edit_SetTabStops_cpp, controls.Edit_SetTabStops, controls._win32_Edit_SetTabStops, windowsx/Edit_SetTabStops
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
 - Edit_SetTabStops
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Edit_SetTabStops macro


## -description


Sets the tab stops in a multiline edit or rich edit control. When text is copied to the control, any tab character in the text causes space to be generated up to the next tab stop. You can use this macro or send the <a href="https://msdn.microsoft.com/d6fe2828-4ae9-4652-ace0-2f71e146f777">EM_SETTABSTOPS</a> message explicitly.


## -parameters




### -param hwndCtl

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the control.


### -param cTabs

Type: <b>int</b>

The number of tab stops contained in the array. If this parameter is zero, the <i>lpTabs</i> parameter is ignored and default tab stops are set at every 32 dialog template units. If this parameter is 1, tab stops are set at every <i>n</i> dialog template units, where <i>n</i> is the distance pointed to by the <i>lpTabs</i> parameter. If this parameter is greater than 1, <i>lpTabs</i> is a pointer to an array of tab stops. 



### -param lpTabs

Type: <b>int*</b>

A pointer to an array of unsigned integers specifying the tab stops, in dialog template units. If <i>cTabs</i> is 1, this parameter is a pointer to an unsigned integer containing the distance between all tab stops, in dialog template units. 


## -remarks



For more information, see <a href="https://msdn.microsoft.com/d6fe2828-4ae9-4652-ace0-2f71e146f777">EM_SETTABSTOPS</a>.



