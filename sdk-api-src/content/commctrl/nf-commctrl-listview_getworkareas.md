---
UID: NF:commctrl.ListView_GetWorkAreas
title: ListView_GetWorkAreas macro (commctrl.h)
author: windows-sdk-content
description: Gets the working areas from a list-view control. You can use this macro, or send the LVM_GETWORKAREAS message explicitly.
old-location: controls\ListView_GetWorkAreas.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getworkareas.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ListView_GetWorkAreas, ListView_GetWorkAreas macro [Windows Controls], _win32_ListView_GetWorkAreas, _win32_ListView_GetWorkAreas_cpp, commctrl/ListView_GetWorkAreas, controls.ListView_GetWorkAreas, controls._win32_ListView_GetWorkAreas
ms.topic: macro
f1_keywords: ["commctrl/ListView_GetWorkAreas"]
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
 - ListView_GetWorkAreas
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ListView_GetWorkAreas macro


## -description


Gets the working areas from a list-view control. You can use this macro, or send the <a href="https://docs.microsoft.com/windows/desktop/Controls/lvm-getworkareas">LVM_GETWORKAREAS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list-view control. 


### -param nWorkAreas

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">INT</a></b>

The number of <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures in the array at <i>lprc</i>. 


### -param prc

Type: <b>LPRECT</b>

A pointer to an array of <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structures that receive the working areas of the list-view control. Values in these structures are in client coordinates. <i>nWorkAreas</i>  specifies the number of structures in this array. 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Controls/using-list-view-controls">Using List-View Controls</a>
 

 

