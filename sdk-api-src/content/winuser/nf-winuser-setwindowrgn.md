---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# SetWindowRgn function


## -description


The <b>SetWindowRgn</b> function sets the window region of a window. The window region determines the area within the window where the system permits drawing. The system does not display any portion of a window that lies outside of the window region


## -parameters




### -param hWnd [in]

A handle to the window whose window region is to be set.


### -param hRgn [in]

A handle to a region. The function sets the window region of the window to this region.

If <i>hRgn</i> is <b>NULL</b>, the function sets the window region to <b>NULL</b>.


### -param bRedraw [in]

Specifies whether the system redraws the window after setting the window region. If <i>bRedraw</i> is <b>TRUE</b>, the system does so; otherwise, it does not.

Typically, you set <i>bRedraw</i> to <b>TRUE</b> if the window is visible.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -remarks



When this function is called, the system sends the <a href="_win32_wm_windowposchanging_cpp">WM_WINDOWPOSCHANGING</a> and <b>WM_WINDOWPOSCHANGING</b> messages to the window.

The coordinates of a window's window region are relative to the upper-left corner of the window, not the client area of the window.

<div class="alert"><b>Note</b>  If the window layout is right-to-left (RTL), the coordinates are relative to the upper-right corner of the window. See <a href="_win32_Window_Features">Window Layout and Mirroring</a>.</div>
<div> </div>
After a successful call to <b>SetWindowRgn</b>, the system owns the region specified by the region handle <i>hRgn</i>. The system does not make a copy of the region. Thus, you should not make any further function calls with this region handle. In particular, do not delete this region handle. The system deletes the region handle when it no longer needed.

To obtain the window region of a window, call the <a href="https://msdn.microsoft.com/c8a8fa46-354b-489e-b016-fd2e728958ce">GetWindowRgn</a> function.




## -see-also




<a href="https://msdn.microsoft.com/c8a8fa46-354b-489e-b016-fd2e728958ce">GetWindowRgn</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>



<a href="_win32_wm_windowposchanging_cpp">WM_WINDOWPOSCHANGING</a>
 

 

