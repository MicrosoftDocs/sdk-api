---
UID: NF:commctrl.ListView_GetColumn
title: ListView_GetColumn macro
author: windows-sdk-content
description: Gets the attributes of a list-view control's column. You can use this macro or send the LVM_GETCOLUMN message explicitly.
old-location: controls\ListView_GetColumn.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getcolumn.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ListView_GetColumn, ListView_GetColumn macro [Windows Controls], _win32_ListView_GetColumn, _win32_ListView_GetColumn_cpp, commctrl/ListView_GetColumn, controls.ListView_GetColumn, controls._win32_ListView_GetColumn
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
 - ListView_GetColumn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- HeaderDef
: 
- commctrl.h
: 
- ListView_GetColumn
: 
---

# ListView_GetColumn macro


## -description


Gets the attributes of a list-view control's column. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb774911(v=VS.85).aspx">LVM_GETCOLUMN</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list-view control. 


### -param iCol

Type: <b>int</b>

The index of the column. 


### -param pcol

Type: <b>LPLVCOLUMN</b>

A pointer to an <a href="https://msdn.microsoft.com/en-us/library/Bb774743(v=VS.85).aspx">LVCOLUMN</a> structure that specifies the information to retrieve and receives information about the column. The 
<b>mask</b> member specifies which column attributes to retrieve. If the <b>mask</b> member specifies the LVCF_TEXT value, the <b>pszText</b> member must contain the address of the buffer that receives the item text, and the <b>cchTextMax</b> member must specify the size of the buffer.

