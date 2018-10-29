---
UID: NF:commctrl.ImageList_AddMasked
title: ImageList_AddMasked function
author: windows-sdk-content
description: Adds an image or images to an image list, generating a mask from the specified bitmap.
old-location: controls\ImageList_AddMasked.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_addmasked.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ImageList_AddMasked, ImageList_AddMasked function [Windows Controls], _win32_ImageList_AddMasked, _win32_ImageList_AddMasked_cpp, commctrl/ImageList_AddMasked, controls.ImageList_AddMasked, controls._win32_ImageList_AddMasked
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
 - Ext-MS-Win-Shell-ComCtl32-Init-L1-1-1.dll
api_name:
 - ImageList_AddMasked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_AddMasked function


## -description


Adds an image or images to an image list, generating a mask from the specified bitmap.


## -parameters




### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list.


### -param hbmImage

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HBITMAP</a></b>

A handle to the bitmap that contains one or more images. The number of images is inferred from the width of the bitmap.


### -param crMask

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">COLORREF</a></b>

The color used to generate the mask. Each pixel of this color in the specified bitmap is changed to black, and the corresponding bit in the mask is set to 1.


## -returns



Type: <b>int</b>

Returns the index of the first new image if successful, or -1 otherwise.




## -remarks



The <b>ImageList_AddMasked</b> function copies the bitmap to an internal data structure. Bitmaps with color depth greater than 8bpp are not supported. Be sure to use the <a href="https://msdn.microsoft.com/en-us/library/Dd183539(v=VS.85).aspx">DeleteObject</a> function to delete <i>hbmImage</i> after the function returns.



