---
UID: NF:commctrl.ListView_SetToolTips
title: ListView_SetToolTips macro
author: windows-driver-content
description: Sets the tooltip control that the list-view control will use to display tooltips. You can use this macro or send the LVM_SETTOOLTIPS message explicitly.
old-location: controls\ListView_SetToolTips.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settooltips.htm
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ListView_SetToolTips, ListView_SetToolTips macro [Windows Controls], _win32_ListView_SetToolTips, _win32_ListView_SetToolTips_cpp, commctrl/ListView_SetToolTips, controls.ListView_SetToolTips, controls._win32_ListView_SetToolTips
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Commctrl.h
api_name:
-	ListView_SetToolTips
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetToolTips macro


## -description


Sets the tooltip control that the list-view control will use to display tooltips. You can use this macro or send the <a href="https://msdn.microsoft.com/5b4335a4-e9f0-4b13-b00b-516af3b60bf1">LVM_SETTOOLTIPS</a> message explicitly. 


## -parameters




### -param hwndLV

TBD


### -param hwndNewHwnd

TBD






#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


#### - hwndToolTip

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the tooltip control to be set. 


## -see-also




<a href="https://msdn.microsoft.com/3d8277a6-e35d-4b07-9817-d13b42a66fe6">ListView_GetToolTips</a>
 

 

