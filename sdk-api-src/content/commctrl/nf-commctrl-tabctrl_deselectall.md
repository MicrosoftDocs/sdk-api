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



