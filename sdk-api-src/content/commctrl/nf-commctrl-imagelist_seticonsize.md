---
UID: NF:commctrl.ImageList_SetIconSize
title: ImageList_SetIconSize function
author: windows-sdk-content
description: Sets the dimensions of images in an image list and removes all images from the list.
old-location: controls\ImageList_SetIconSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_seticonsize.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ImageList_SetIconSize, ImageList_SetIconSize function [Windows Controls], _win32_ImageList_SetIconSize, _win32_ImageList_SetIconSize_cpp, commctrl/ImageList_SetIconSize, controls.ImageList_SetIconSize, controls._win32_ImageList_SetIconSize
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
 - ImageList_SetIconSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ImageList_SetIconSize
: 
---

# ImageList_SetIconSize function


## -description


Sets the dimensions of images in an image list and removes all images from the list. 


## -parameters




### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param cx

Type: <b>int</b>

The width, in pixels, of the images in the image list. All images in an image list have the same dimensions. 


### -param cy

Type: <b>int</b>

The height, in pixels, of the images in the image list. All images in an image list have the same dimensions. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.



