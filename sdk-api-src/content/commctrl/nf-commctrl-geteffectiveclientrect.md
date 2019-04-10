---
UID: NF:commctrl.GetEffectiveClientRect
title: GetEffectiveClientRect function (commctrl.h)
author: windows-sdk-content
description: Calculates the dimensions of a rectangle in the client area that contains all the specified controls.
old-location: controls\GetEffectiveClientRect.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\common\functions\geteffectiveclientrect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetEffectiveClientRect, GetEffectiveClientRect function [Windows Controls], _win32_GetEffectiveClientRect, _win32_GetEffectiveClientRect_cpp, commctrl/GetEffectiveClientRect, controls.GetEffectiveClientRect, controls._win32_GetEffectiveClientRect
ms.topic: function
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - GetEffectiveClientRect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetEffectiveClientRect function


## -description


Calculates the dimensions of a rectangle in the client area that contains all the specified controls. 


## -parameters




### -param hWnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window that has the client area to check. 


### -param lprc

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that receives the dimensions of the rectangle. 


### -param lpInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a>*</b>

A pointer to a null-terminated array of integers that identify controls in the client area. Each control requires a pair of consecutive elements. The first element of the pair must be nonzero and the second element of the pair must be the control identifier. The first pair represents the menu and is ignored. The last element must be zero to identify the end of the array. 


## -returns



No return value. 




## -remarks



If a window in the <i>lprc</i> array is visible, or will be visible when its parent becomes visible, its rectangle is subtracted from the effective client rectangle.  
	




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb775731(v=VS.85).aspx">ShowHideMenuCtl</a>
 

 

