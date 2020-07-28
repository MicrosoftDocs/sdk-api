---
UID: NF:commctrl.ListView_GetColumnOrderArray
title: ListView_GetColumnOrderArray macro (commctrl.h)
description: Gets the current left-to-right order of columns in a list-view control. You can use this macro or send the LVM_GETCOLUMNORDERARRAY message explicitly.
helpviewer_keywords: ["ListView_GetColumnOrderArray","ListView_GetColumnOrderArray macro [Windows Controls]","_win32_ListView_GetColumnOrderArray","_win32_ListView_GetColumnOrderArray_cpp","commctrl/ListView_GetColumnOrderArray","controls.ListView_GetColumnOrderArray","controls._win32_ListView_GetColumnOrderArray"]
old-location: controls\ListView_GetColumnOrderArray.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcolumnorderarray.htm
ms.date: 12/05/2018
ms.keywords: ListView_GetColumnOrderArray, ListView_GetColumnOrderArray macro [Windows Controls], _win32_ListView_GetColumnOrderArray, _win32_ListView_GetColumnOrderArray_cpp, commctrl/ListView_GetColumnOrderArray, controls.ListView_GetColumnOrderArray, controls._win32_ListView_GetColumnOrderArray
f1_keywords:
- commctrl/ListView_GetColumnOrderArray
dev_langs:
- c++
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
- ListView_GetColumnOrderArray
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetColumnOrderArray macro


## -description


Gets the current left-to-right order of columns in a list-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getcolumnorderarray">LVM_GETCOLUMNORDERARRAY</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to a list-view control. 


### -param iCount

Type: <b>int</b>

The number of columns in the list-view control.


### -param pi

Type: <b>int*</b>

A pointer to an array of integers that will receive the index values of the columns in the list-view control. The array must be large enough to hold 
					<i>iCount</i> elements. 

