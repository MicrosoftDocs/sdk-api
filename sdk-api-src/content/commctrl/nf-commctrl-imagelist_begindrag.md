---
UID: NF:commctrl.ImageList_BeginDrag
title: ImageList_BeginDrag function
author: windows-sdk-content
description: Begins dragging an image.
old-location: controls\ImageList_BeginDrag.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_begindrag.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ImageList_BeginDrag, ImageList_BeginDrag function [Windows Controls], _win32_ImageList_BeginDrag, _win32_ImageList_BeginDrag_cpp, commctrl/ImageList_BeginDrag, controls.ImageList_BeginDrag, controls._win32_ImageList_BeginDrag
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
 - ImageList_BeginDrag
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# ImageList_BeginDrag function


## -description


Begins dragging an image. 


## -parameters




### -param himlTrack

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param iTrack

Type: <b>int</b>

The index of the image to drag. 


### -param dxHotspot

Type: <b>int</b>

The x-coordinate of the location of the drag position relative to the upper-left corner of the image. 


### -param dyHotspot

Type: <b>int</b>

The y-coordinate of the location of the drag position relative to the upper-left corner of the image. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 




## -remarks



This function creates a temporary image list that is used for dragging. In response to subsequent <a href="https://msdn.microsoft.com/en-us/library/ms645616(v=VS.85).aspx">WM_MOUSEMOVE</a> messages, you can move the drag image by using the <a href="https://msdn.microsoft.com/en-us/library/Bb761530(v=VS.85).aspx">ImageList_DragMove</a> function. To end the drag operation, you can use the <a href="https://msdn.microsoft.com/en-us/library/Bb761541(v=VS.85).aspx">ImageList_EndDrag</a> function. 



