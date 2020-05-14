---
UID: NF:commctrl.ListView_GetNumberOfWorkAreas
title: ListView_GetNumberOfWorkAreas macro (commctrl.h)
description: Gets the number of working areas in a list-view control. You can use this macro or send the LVM_GETNUMBEROFWORKAREAS message explicitly.helpviewer_keywords: ["ListView_GetNumberOfWorkAreas","ListView_GetNumberOfWorkAreas macro [Windows Controls]","_win32_ListView_GetNumberOfWorkAreas","_win32_ListView_GetNumberOfWorkAreas_cpp","commctrl/ListView_GetNumberOfWorkAreas","controls.ListView_GetNumberOfWorkAreas","controls._win32_ListView_GetNumberOfWorkAreas"]
old-location: controls\ListView_GetNumberOfWorkAreas.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getnumberofworkareas.htm
ms.date: 12/05/2018
ms.keywords: ListView_GetNumberOfWorkAreas, ListView_GetNumberOfWorkAreas macro [Windows Controls], _win32_ListView_GetNumberOfWorkAreas, _win32_ListView_GetNumberOfWorkAreas_cpp, commctrl/ListView_GetNumberOfWorkAreas, controls.ListView_GetNumberOfWorkAreas, controls._win32_ListView_GetNumberOfWorkAreas
f1_keywords:
- commctrl/ListView_GetNumberOfWorkAreas
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
- ListView_GetNumberOfWorkAreas
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetNumberOfWorkAreas macro


## -description


Gets the number of working areas in a list-view control. You can use this macro or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getnumberofworkareas">LVM_GETNUMBEROFWORKAREAS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param pnWorkAreas

Type: <b>LPUINT</b>

A pointer to a UINT value that receives the number of working areas in the list-view control. If zero is placed in this variable, then no working areas are currently set. This value cannot be <b>NULL</b>. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/using-list-view-controls">Using List-View Controls</a>
 

 

