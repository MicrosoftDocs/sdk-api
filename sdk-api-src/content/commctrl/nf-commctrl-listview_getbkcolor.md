---
UID: NF:commctrl.ListView_GetBkColor
title: ListView_GetBkColor macro
author: windows-driver-content
description: Gets the background color of a list-view control. You can use this macro or send the LVM_GETBKCOLOR message explicitly.
old-location: controls\ListView_GetBkColor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getbkcolor.htm
ms.author: windowsdriverdev
ms.date: 4/27/2018
ms.keywords: ListView_GetBkColor, ListView_GetBkColor macro [Windows Controls], _win32_ListView_GetBkColor, _win32_ListView_GetBkColor_cpp, commctrl/ListView_GetBkColor, controls.ListView_GetBkColor, controls._win32_ListView_GetBkColor
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
-	ListView_GetBkColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetBkColor macro


## -description


Gets the background color of a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/077d3b2e-f6d1-4acc-b002-e9e707ad274c">LVM_GETBKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 

