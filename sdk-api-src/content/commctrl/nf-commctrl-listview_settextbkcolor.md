---
UID: NF:commctrl.ListView_SetTextBkColor
title: ListView_SetTextBkColor macro (commctrl.h)
author: windows-sdk-content
description: Sets the background color of text in a list-view control. You can use this macro or send the LVM_SETTEXTBKCOLOR message explicitly.
old-location: controls\ListView_SetTextBkColor.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settextbkcolor.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_SetTextBkColor, ListView_SetTextBkColor macro [Windows Controls], _win32_ListView_SetTextBkColor, _win32_ListView_SetTextBkColor_cpp, commctrl/ListView_SetTextBkColor, controls.ListView_SetTextBkColor, controls._win32_ListView_SetTextBkColor
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
 - ListView_SetTextBkColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_SetTextBkColor macro


## -description


Sets the background color of text in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761206(v=VS.85).aspx">LVM_SETTEXTBKCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param clrTextBk

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

The new text background color. This can be CLR_NONE for no background color.

