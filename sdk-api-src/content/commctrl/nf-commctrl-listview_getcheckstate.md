---
UID: NF:commctrl.ListView_GetCheckState
title: ListView_GetCheckState macro
author: windows-driver-content
description: Determines if an item in a list-view control is selected. This should be used only for list-view controls that have the LVS_EX_CHECKBOXES style.
old-location: controls\ListView_GetCheckState.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcheckstate.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ListView_GetCheckState, ListView_GetCheckState macro [Windows Controls], _win32_ListView_GetCheckState, _win32_ListView_GetCheckState_cpp, commctrl/ListView_GetCheckState, controls.ListView_GetCheckState, controls._win32_ListView_GetCheckState
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
-	ListView_GetCheckState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetCheckState macro


## -description


Determines if an item in a list-view control is selected. This should be used only for list-view controls that have the <a href="Extended_list_view_styles.htm">LVS_EX_CHECKBOXES</a> style. 


## -parameters




### -param hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


### -param i

TBD






#### - iIndex

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

The index of the item for which to retrieve the check state. 

