---
UID: NF:commctrl.ListView_SetTextColor
title: ListView_SetTextColor macro
author: windows-sdk-content
description: Sets the text color of a list-view control. You can use this macro or send the LVM_SETTEXTCOLOR message explicitly.
old-location: controls\ListView_SetTextColor.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_settextcolor.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListView_SetTextColor, ListView_SetTextColor macro [Windows Controls], _win32_ListView_SetTextColor, _win32_ListView_SetTextColor_cpp, commctrl/ListView_SetTextColor, controls.ListView_SetTextColor, controls._win32_ListView_SetTextColor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: macro
req.header: commctrl.h
req.include-header: 
req.redist: 
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
 - ListView_SetTextColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_SetTextColor macro


## -description


Sets the text color of a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761208(v=VS.85).aspx">LVM_SETTEXTCOLOR</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control. 


### -param clrText

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">COLORREF</a></b>

The new text color. 

