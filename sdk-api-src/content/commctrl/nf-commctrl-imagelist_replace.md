---
UID: NF:commctrl.ImageList_Replace
title: ImageList_Replace function
author: windows-sdk-content
description: Replaces an image in an image list with a new image.
old-location: controls\ImageList_Replace.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_replace.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ImageList_Replace, ImageList_Replace function [Windows Controls], _win32_ImageList_Replace, _win32_ImageList_Replace_cpp, commctrl/ImageList_Replace, controls.ImageList_Replace, controls._win32_ImageList_Replace
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
 - ImageList_Replace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ImageList_Replace function


## -description


Replaces an image in an image list with a new image. 


## -parameters




### -param himl

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param i

Type: <b>int</b>

An index of the image to replace. 


### -param hbmImage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a></b>

A handle to the bitmap that contains the image. 


### -param hbmMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HBITMAP</a></b>

A handle to the bitmap that contains the mask. If no mask is used with the image list, this parameter is ignored. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise. 




## -remarks



The <b>ImageList_Replace</b> function copies the bitmap to an internal data structure. Be sure to use the <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> function to delete <i>hbmImage</i> and <i>hbmMask</i> after the function returns. 



