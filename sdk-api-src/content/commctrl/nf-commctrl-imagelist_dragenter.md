---
UID: NF:commctrl.ImageList_DragEnter
title: ImageList_DragEnter function
author: windows-driver-content
description: Displays the drag image at the specified position within the window.
old-location: controls\ImageList_DragEnter.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_dragenter.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: ImageList_DragEnter, ImageList_DragEnter function [Windows Controls], _win32_ImageList_DragEnter, _win32_ImageList_DragEnter_cpp, commctrl/ImageList_DragEnter, controls.ImageList_DragEnter, controls._win32_ImageList_DragEnter
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Comctl32.dll
api_name:
-	ImageList_DragEnter
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# ImageList_DragEnter function


## -description


Displays the drag image at the specified position within the window. 


## -parameters




### -param hwndLock

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the window that owns the drag image. 


### -param x

Type: <b>int</b>

The x-coordinate at which to display the drag image. The coordinate is relative to the upper-left corner of the window, not the client area. 


### -param y

Type: <b>int</b>

The y-coordinate at which to display the drag image. The coordinate is relative to the upper-left corner of the window, not the client area. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 




## -remarks



To begin a drag operation, use the <a href="https://msdn.microsoft.com/5b262b32-5ec2-4f19-8a76-4c318aec7dc7">ImageList_BeginDrag</a> function. 



