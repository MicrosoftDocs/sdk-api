---
UID: NF:commctrl.LBItemFromPt
title: LBItemFromPt function
author: windows-sdk-content
description: Retrieves the index of the item at the specified point in a list box.
old-location: controls\LBItemFromPt.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\draglb\functions\lbitemfrompt.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: LBItemFromPt, LBItemFromPt function [Windows Controls], _win32_LBItemFromPt, _win32_LBItemFromPt_cpp, commctrl/LBItemFromPt, controls.LBItemFromPt, controls._win32_LBItemFromPt
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - LBItemFromPt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- LBItemFromPt
: 
---

# LBItemFromPt function


## -description


Retrieves the index of the item at the specified point in a list box. 


## -parameters




### -param hLB

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HWND</a></b>

A handle to the list box to check. 


### -param pt

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

A <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that contains the screen coordinates to check. 


### -param bAutoScroll

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

A scroll flag. If this parameter is <b>TRUE</b> and the point is directly above or below the list box, the function scrolls the list box by one line and returns -1. Otherwise, the function does not scroll the list box. 


## -returns



Type: <b>int</b>

Returns the item identifier if the point is over a list item, or -1 otherwise. 




## -remarks



The <b>LBItemFromPt</b> function only scrolls the list box if a minimum amount of time has passed since it last did so. Timing prevents the list box from scrolling too quickly if the function is called repeatedly in rapid succession—for example, when <a href="https://msdn.microsoft.com/en-us/library/Bb761721(v=VS.85).aspx">DL_DRAGGING</a> notification codes or <a href="https://msdn.microsoft.com/en-us/library/ms645616(v=VS.85).aspx">WM_MOUSEMOVE</a> messages are processed. 

If the specified point is outside the client area of the list box and 
				<i>bAutoScroll</i> is <b>TRUE</b>, the function scrolls the list box instead of returning an item identifier. 



