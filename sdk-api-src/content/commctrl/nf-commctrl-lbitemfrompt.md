---
UID: NF:commctrl.LBItemFromPt
title: LBItemFromPt function
author: windows-sdk-content
description: Retrieves the index of the item at the specified point in a list box.
old-location: controls\LBItemFromPt.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\draglb\functions\lbitemfrompt.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: LBItemFromPt, LBItemFromPt function [Windows Controls], _win32_LBItemFromPt, _win32_LBItemFromPt_cpp, commctrl/LBItemFromPt, controls.LBItemFromPt, controls._win32_LBItemFromPt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: commctrl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: STGOPTIONS
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# LBItemFromPt function


## -description


Retrieves the index of the item at the specified point in a list box. 


## -parameters




### -param hLB

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list box to check. 


### -param pt

Type: <b><a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a></b>

A <a href="https://msdn.microsoft.com/ecb0f0e1-90c2-48ab-a069-552262b49c7c">POINT</a> structure that contains the screen coordinates to check. 


### -param bAutoScroll

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A scroll flag. If this parameter is <b>TRUE</b> and the point is directly above or below the list box, the function scrolls the list box by one line and returns -1. Otherwise, the function does not scroll the list box. 


## -returns



Type: <b>int</b>

Returns the item identifier if the point is over a list item, or -1 otherwise. 




## -remarks



The <b>LBItemFromPt</b> function only scrolls the list box if a minimum amount of time has passed since it last did so. Timing prevents the list box from scrolling too quickly if the function is called repeatedly in rapid succession—for example, when <a href="https://msdn.microsoft.com/87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7">DL_DRAGGING</a> notification codes or <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a> messages are processed. 

If the specified point is outside the client area of the list box and 
				<i>bAutoScroll</i> is <b>TRUE</b>, the function scrolls the list box instead of returning an item identifier. 



