---
UID: NF:commctrl.ListView_SetWorkAreas
title: ListView_SetWorkAreas macro
author: windows-sdk-content
description: Sets the working areas within a list-view control. You can use this macro or send the LVM_SETWORKAREAS message explicitly.
old-location: controls\ListView_SetWorkAreas.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\listview\macros\listview_setworkareas.htm
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ListView_SetWorkAreas, ListView_SetWorkAreas macro [Windows Controls], _win32_ListView_SetWorkAreas, _win32_ListView_SetWorkAreas_cpp, commctrl/ListView_SetWorkAreas, controls.ListView_SetWorkAreas, controls._win32_ListView_SetWorkAreas
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
 - ListView_SetWorkAreas
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ListView_SetWorkAreas macro


## -description


Sets the working areas within a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/en-us/library/Bb761223(v=VS.85).aspx">LVM_SETWORKAREAS</a> message explicitly. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to a list-view control. 


### -param nWorkAreas

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The number of <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structures in the array at 
					<i>lprc</i>. The maximum number of working areas allowed is defined by the <b>LV_MAX_WORKAREAS</b> value.


### -param prc

Type: <b>LPRECT</b>

A pointer to an array of <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structures that contain the new working areas of the list-view control. Values in these structures are in client coordinates. If this parameter is <b>NULL</b>, the working area will be set to the client area of the control. <i>nWorkAreas</i> specifies the number of structures in this array. 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb774736(v=VS.85).aspx">Using List-View Controls</a>
 

 

