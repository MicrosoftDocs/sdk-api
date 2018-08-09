---
UID: NF:commctrl.ListView_GetColumnWidth
title: ListView_GetColumnWidth macro
author: windows-sdk-content
description: Gets the width of a column in report or list view. You can use this macro or send the LVM_GETCOLUMNWIDTH message explicitly.
old-location: controls\ListView_GetColumnWidth.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcolumnwidth.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ListView_GetColumnWidth, ListView_GetColumnWidth macro [Windows Controls], _win32_ListView_GetColumnWidth, _win32_ListView_GetColumnWidth_cpp, commctrl/ListView_GetColumnWidth, controls.ListView_GetColumnWidth, controls._win32_ListView_GetColumnWidth
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
 - ListView_GetColumnWidth
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ListView_GetColumnWidth macro


## -description


Gets the width of a column in report or list view. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774915(v=VS.85).aspx">LVM_GETCOLUMNWIDTH</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param iCol

Type: <b>int</b>

The index of the column. This parameter is ignored in list view. 

