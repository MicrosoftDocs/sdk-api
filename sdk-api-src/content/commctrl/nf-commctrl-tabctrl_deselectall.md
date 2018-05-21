---
UID: NF:commctrl.TabCtrl_DeselectAll
title: TabCtrl_DeselectAll macro
author: windows-driver-content
description: Resets items in a tab control, clearing any that were set to the TCIS_BUTTONPRESSED state. You can use this macro or send the TCM_DESELECTALL message explicitly.
old-location: controls\TabCtrl_DeselectAll.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_deselectall.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: TabCtrl_DeselectAll, TabCtrl_DeselectAll macro [Windows Controls], _win32_TabCtrl_DeselectAll, _win32_TabCtrl_DeselectAll_cpp, commctrl/TabCtrl_DeselectAll, controls.TabCtrl_DeselectAll, controls._win32_TabCtrl_DeselectAll
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
-	TabCtrl_DeselectAll
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# TabCtrl_DeselectAll macro


## -description


Resets items in a tab control, clearing any that were set to the <a href="Tab_Control_Item_States.htm">TCIS_BUTTONPRESSED</a> state. You can use this macro or send the <a href="https://msdn.microsoft.com/cc2e5131-3c1b-473a-a0ca-274a2d39a2f1">TCM_DESELECTALL</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param fExcludeFocus

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Flag value that specifies the scope of the item deselection. If this parameter is set to <b>FALSE</b>, all tab items will be reset. If it is set to <b>TRUE</b>, all but the currently selected tab item will be reset. 


#### - hwndTab

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


## -remarks



This message is only meaningful if the <a href="Tab_Control_Styles.htm">TCS_BUTTONS</a> style flag has been set. 



