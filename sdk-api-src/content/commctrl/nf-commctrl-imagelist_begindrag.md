---
UID: NF:commctrl.ImageList_BeginDrag
title: ImageList_BeginDrag function
author: windows-driver-content
description: Begins dragging an image.
old-location: controls\ImageList_BeginDrag.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_begindrag.htm
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: ImageList_BeginDrag, ImageList_BeginDrag function [Windows Controls], _win32_ImageList_BeginDrag, _win32_ImageList_BeginDrag_cpp, commctrl/ImageList_BeginDrag, controls.ImageList_BeginDrag, controls._win32_ImageList_BeginDrag
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
-	ImageList_BeginDrag
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



This function creates a temporary image list that is used for dragging. In response to subsequent <a href="https://msdn.microsoft.com/9b99387e-e176-4b20-a05a-bc75928a1367">WM_MOUSEMOVE</a> messages, you can move the drag image by using the <a href="https://msdn.microsoft.com/a7d7fcd4-ba03-43ba-ae37-df8d4173c64d">ImageList_DragMove</a> function. To end the drag operation, you can use the <a href="https://msdn.microsoft.com/54465b0d-6bbe-4c50-8124-cbf3115d0848">ImageList_EndDrag</a> function. 



