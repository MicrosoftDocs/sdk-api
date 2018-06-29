---
UID: NF:commctrl.ListView_GetHotCursor
title: ListView_GetHotCursor macro
author: windows-sdk-content
description: Gets the HCURSOR used when the pointer is over an item while hot tracking is enabled. You can use this macro or send the LVM_GETHOTCURSOR message explicitly.
old-location: controls\ListView_GetHotCursor.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_gethotcursor.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ListView_GetHotCursor, ListView_GetHotCursor macro [Windows Controls], _win32_ListView_GetHotCursor, _win32_ListView_GetHotCursor_cpp, commctrl/ListView_GetHotCursor, controls.ListView_GetHotCursor, controls._win32_ListView_GetHotCursor
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: STGOPTIONS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ListView_GetHotCursor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetHotCursor macro


## -description


Gets the HCURSOR used when the pointer is over an item while hot tracking is enabled. You can use this macro or send the <a href="https://msdn.microsoft.com/library/Bb774938(v=VS.85).aspx">LVM_GETHOTCURSOR</a> message explicitly. 


## -parameters




### -param hwnd

TBD






#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a list-view control. 


## -remarks



A list-view control uses hot tracking and hover selection when the <a href="https://msdn.microsoft.com/library/Bb774732(v=VS.85).aspx">LVS_EX_TRACKSELECT</a> style is set. 



