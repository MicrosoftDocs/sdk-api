---
UID: NF:commctrl.ListView_GetWorkAreas
title: ListView_GetWorkAreas macro (commctrl.h)
author: windows-sdk-content
description: Gets the working areas from a list-view control. You can use this macro, or send the LVM_GETWORKAREAS message explicitly.
old-location: controls\ListView_GetWorkAreas.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_getworkareas.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ListView_GetWorkAreas, ListView_GetWorkAreas macro [Windows Controls], _win32_ListView_GetWorkAreas, _win32_ListView_GetWorkAreas_cpp, commctrl/ListView_GetWorkAreas, controls.ListView_GetWorkAreas, controls._win32_ListView_GetWorkAreas
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
 - ListView_GetWorkAreas
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_GetWorkAreas macro


## -description


Gets the working areas from a list-view control. You can use this macro, or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761095(v=VS.85).aspx">LVM_GETWORKAREAS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


### -param nWorkAreas

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The number of <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structures in the array at <i>lprc</i>. 


### -param prc

Type: <b>LPRECT</b>

A pointer to an array of <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structures that receive the working areas of the list-view control. Values in these structures are in client coordinates. <i>nWorkAreas</i>  specifies the number of structures in this array. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774736(v=VS.85).aspx">Using List-View Controls</a>
 

 

