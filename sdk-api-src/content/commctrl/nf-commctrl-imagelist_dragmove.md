---
UID: NF:commctrl.ImageList_DragMove
title: ImageList_DragMove function
author: windows-sdk-content
description: Moves the image that is being dragged during a drag-and-drop operation. This function is typically called in response to a WM_MOUSEMOVE message.
old-location: controls\ImageList_DragMove.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_dragmove.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ImageList_DragMove, ImageList_DragMove function [Windows Controls], _win32_ImageList_DragMove, _win32_ImageList_DragMove_cpp, commctrl/ImageList_DragMove, controls.ImageList_DragMove, controls._win32_ImageList_DragMove
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
 - ImageList_DragMove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_DragMove function


## -description


Moves the image that is being dragged during a drag-and-drop operation. This function is typically called in response to a <a href="https://msdn.microsoft.com/en-us/library/ms645616(v=VS.85).aspx">WM_MOUSEMOVE</a> message. 


## -parameters




### -param x

Type: <b>int</b>

The x-coordinate at which to display the drag image. The coordinate is relative to the upper-left corner of the window, not the client area. 


### -param y

Type: <b>int</b>

The y-coordinate at which to display the drag image. The coordinate is relative to the upper-left corner of the window, not the client area. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 




## -remarks



To begin a drag operation, use the <a href="https://msdn.microsoft.com/en-us/library/Bb761516(v=VS.85).aspx">ImageList_BeginDrag</a> function. 



