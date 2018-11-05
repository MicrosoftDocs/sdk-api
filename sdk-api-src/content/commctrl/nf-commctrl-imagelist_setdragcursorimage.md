---
UID: NF:commctrl.ImageList_SetDragCursorImage
title: ImageList_SetDragCursorImage function
author: windows-sdk-content
description: Creates a new drag image by combining the specified image (typically a mouse cursor image) with the current drag image.
old-location: controls\ImageList_SetDragCursorImage.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_setdragcursorimage.htm
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ImageList_SetDragCursorImage, ImageList_SetDragCursorImage function [Windows Controls], _win32_ImageList_SetDragCursorImage, _win32_ImageList_SetDragCursorImage_cpp, commctrl/ImageList_SetDragCursorImage, controls.ImageList_SetDragCursorImage, controls._win32_ImageList_SetDragCursorImage
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
 - ImageList_SetDragCursorImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_SetDragCursorImage function


## -description


Creates a new drag image by combining the specified image (typically a mouse cursor image) with the current drag image. 


## -parameters




### -param himlDrag

Type: <b>HIMAGELIST</b>

A handle to the image list that contains the new image to combine with the drag image.


### -param iDrag

Type: <b>int</b>

The index of the new image to combine with the drag image.


### -param dxHotspot

Type: <b>int</b>

The x-position of the hot spot within the new image.


### -param dyHotspot

Type: <b>int</b>

The y-position of the hot spot within the new image.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.



