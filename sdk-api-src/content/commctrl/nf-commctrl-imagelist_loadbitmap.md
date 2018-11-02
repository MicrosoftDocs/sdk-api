---
UID: NF:commctrl.ImageList_LoadBitmap
title: ImageList_LoadBitmap macro
author: windows-sdk-content
description: Calls the ImageList_LoadImage function to create an image list from the specified bitmap resource.
old-location: controls\ImageList_LoadBitmap.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\imagelist\macros\imagelist_loadbitmap.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ImageList_LoadBitmap, ImageList_LoadBitmap macro [Windows Controls], _win32_ImageList_LoadBitmap, _win32_ImageList_LoadBitmap_cpp, commctrl/ImageList_LoadBitmap, controls.ImageList_LoadBitmap, controls._win32_ImageList_LoadBitmap
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Commctrl.h
api_name:
 - ImageList_LoadBitmap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_LoadBitmap macro


## -description


Calls the <a href="https://msdn.microsoft.com/en-us/library/Bb761557(v=VS.85).aspx">ImageList_LoadImage</a> function to create an image list from the specified bitmap resource. 


## -parameters




### -param hi

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HINSTANCE</a></b>

A handle to the instance that contains the bitmap resource. This parameter is <b>NULL</b> if you are loading an OEM bitmap. 


### -param lpbmp

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">LPCTSTR</a></b>

The image to load. If the <i>hi</i> parameter is non-<b>NULL</b>, <i>lpbmp</i>is the address of a null-terminated string that contains the name of the image resource in the <i>hi</i> module. If <i>hi</i> is <b>NULL</b>, the <a href="https://msdn.microsoft.com/en-us/library/ms632659(v=VS.85).aspx">LOWORD</a> of this parameter must be the identifier of an OEM bitmap to load. To create this value, use the <a href="https://msdn.microsoft.com/en-us/library/ms648029(v=VS.85).aspx">MAKEINTRESOURCE</a> macro with one of the OEM bitmap identifiers defined in WINUSER.H. These identifiers have the OBM_ prefix.


### -param cx

Type: <b>int</b>

The width of each image. The height of each image and the initial number of images are inferred by the dimensions of the specified bitmap. 


### -param cGrow

Type: <b>int</b>

The number of images by which the image list can grow when the system needs to make room for new images. This parameter represents the number of new images that the resized image list can contain.


### -param crMask

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">COLORREF</a></b>

The color used to generate a mask. Each pixel of this color in the specified bitmap is changed to black, and the corresponding bit in the mask is set to 1. If this parameter is the CLR_NONE value, no mask is generated. 

