---
UID: NS:winuser.tagMOUSEMOVEPOINT
title: MOUSEMOVEPOINT
author: windows-sdk-content
description: Contains information about the mouse's location in screen coordinates.
old-location: inputdev\mousemovepoint.htm
tech.root: inputdev
ms.assetid: VS|winui|~\winui\windowsuserinterface\userinput\mouseinput\mouseinputreference\mouseinputstructures\mousemovepoint.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPMOUSEMOVEPOINT, *PMOUSEMOVEPOINT, MOUSEMOVEPOINT, MOUSEMOVEPOINT structure [Keyboard and Mouse Input], PMOUSEMOVEPOINT, PMOUSEMOVEPOINT structure pointer [Keyboard and Mouse Input], _win32_MOUSEMOVEPOINT_str, _win32_mousemovepoint_str_cpp, inputdev.mousemovepoint, winui._win32_mousemovepoint_str, winuser/MOUSEMOVEPOINT, winuser/PMOUSEMOVEPOINT"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Winuser.h
api_name:
 - MOUSEMOVEPOINT
product: Windows
targetos: Windows
req.typenames: MOUSEMOVEPOINT, *PMOUSEMOVEPOINT, *LPMOUSEMOVEPOINT
req.redist: 
---

# MOUSEMOVEPOINT structure


## -description


Contains information about the mouse's location in screen coordinates.


## -struct-fields




### -field x

Type: <b>int</b>

The x-coordinate of the mouse. 


### -field y

Type: <b>int</b>

The y-coordinate of the mouse. 


### -field time

Type: <b>DWORD</b>

The time stamp of the mouse coordinate. 


### -field dwExtraInfo

Type: <b>ULONG_PTR</b>

Additional information associated with this coordinate. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms646259(v=VS.85).aspx">GetMouseMovePointsEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms645533(v=VS.85).aspx">Mouse Input</a>



<b>Reference</b>
 

 

