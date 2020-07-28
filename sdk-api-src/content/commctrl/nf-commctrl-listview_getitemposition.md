---
UID: NF:commctrl.ListView_GetItemPosition
title: ListView_GetItemPosition macro (commctrl.h)
description: Gets the position of a list-view item. You can use this macro or explicitly send the LVM_GETITEMPOSITION message.
helpviewer_keywords: ["ListView_GetItemPosition","ListView_GetItemPosition macro [Windows Controls]","_win32_ListView_GetItemPosition","_win32_ListView_GetItemPosition_cpp","commctrl/ListView_GetItemPosition","controls.ListView_GetItemPosition","controls._win32_ListView_GetItemPosition"]
old-location: controls\ListView_GetItemPosition.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getitemposition.htm
ms.date: 12/05/2018
ms.keywords: ListView_GetItemPosition, ListView_GetItemPosition macro [Windows Controls], _win32_ListView_GetItemPosition, _win32_ListView_GetItemPosition_cpp, commctrl/ListView_GetItemPosition, controls.ListView_GetItemPosition, controls._win32_ListView_GetItemPosition
f1_keywords:
- commctrl/ListView_GetItemPosition
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
- ListView_GetItemPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetItemPosition macro


## -description


Gets the position of a list-view item. You can use this macro or explicitly send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getitemposition">LVM_GETITEMPOSITION</a> message. 


## -parameters




### -param hwndLV

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param i

Type: <b>int</b>

The index of the list-view item. 


### -param ppt

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a>*</b>

A pointer to a <a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a> structure that receives the position of the item's upper-left corner, in view coordinates. 

