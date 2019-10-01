---
UID: NF:commctrl.ImageList_SetIconSize
title: ImageList_SetIconSize function (commctrl.h)
author: windows-sdk-content
description: Sets the dimensions of images in an image list and removes all images from the list.
old-location: controls\ImageList_SetIconSize.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_seticonsize.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ImageList_SetIconSize, ImageList_SetIconSize function [Windows Controls], _win32_ImageList_SetIconSize, _win32_ImageList_SetIconSize_cpp, commctrl/ImageList_SetIconSize, controls.ImageList_SetIconSize, controls._win32_ImageList_SetIconSize
ms.topic: function
f1_keywords: 
 - "commctrl/ImageList_SetIconSize"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.



