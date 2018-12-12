---
UID: NF:commctrl.TabCtrl_InsertItem
title: TabCtrl_InsertItem macro
author: windows-sdk-content
description: Inserts a new tab in a tab control. You can use this macro or send the TCM_INSERTITEM message explicitly.
old-location: controls\TabCtrl_InsertItem.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\tab\macros\tabctrl_insertitem.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TabCtrl_InsertItem, TabCtrl_InsertItem macro [Windows Controls], _win32_TabCtrl_InsertItem, _win32_TabCtrl_InsertItem_cpp, commctrl/TabCtrl_InsertItem, controls.TabCtrl_InsertItem, controls._win32_TabCtrl_InsertItem
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - TabCtrl_InsertItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TabCtrl_InsertItem macro


## -description


Inserts a new tab in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/e547c49a-699c-4137-8680-20391d138d54">TCM_INSERTITEM</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


### -param iItem

Type: <b>int</b>

Index of the new tab. 


### -param pitem

Type: <b>const LPTCITEM</b>

Pointer to a <a href="https://msdn.microsoft.com/e08c4528-5874-492c-97be-dfdf5f5636a9">TCITEM</a> structure that specifies the attributes of the tab. The <b>dwState</b> and <b>dwStateMask</b> members of this structure are ignored by this message. 

