---
UID: NF:commctrl.ImageList_Add
title: ImageList_Add function
author: windows-sdk-content
description: Adds an image or images to an image list.
old-location: controls\ImageList_Add.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_add.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ImageList_Add, ImageList_Add function [Windows Controls], _win32_ImageList_Add, _win32_ImageList_Add_cpp, commctrl/ImageList_Add, controls.ImageList_Add, controls._win32_ImageList_Add
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
 - ImageList_Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ImageList_Add
: 
---

# ImageList_Add function


## -description


Adds an image or images to an image list. 


## -parameters




### -param himl [in]

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param hbmImage [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HBITMAP</a></b>

A handle to the bitmap that contains the image or images. The number of images is inferred from the width of the bitmap. 


### -param hbmMask [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">HBITMAP</a></b>

A handle to the bitmap that contains the mask. If no mask is used with the image list, this parameter is ignored. This parameter can be <b>NULL</b>.


## -returns



Type: <b>int</b>

Returns the index of the first new image if successful, or -1 otherwise. 




## -remarks



The <b>ImageList_Add</b> function copies the bitmap to an internal data structure. Be sure to use the <a href="https://msdn.microsoft.com/en-us/library/Dd183539(v=VS.85).aspx">DeleteObject</a> function to delete 
				<i>hbmImage</i> and 
				<i>hbmMask</i> after the function returns. 



