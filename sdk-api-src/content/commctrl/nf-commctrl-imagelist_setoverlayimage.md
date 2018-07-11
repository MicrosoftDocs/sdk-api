---
UID: NF:commctrl.ImageList_SetOverlayImage
title: ImageList_SetOverlayImage function
author: windows-sdk-content
description: Adds a specified image to the list of images to be used as overlay masks. An image list can have up to four overlay masks in version 4.70 and earlier and up to 15 in version 4.71. The function assigns an overlay mask index to the specified image.
old-location: controls\ImageList_SetOverlayImage.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\imagelist\functions\imagelist_setoverlayimage.htm
ms.author: windowssdkdev
ms.date: 06/29/2018
ms.keywords: ImageList_SetOverlayImage, ImageList_SetOverlayImage function [Windows Controls], _win32_ImageList_SetOverlayImage, _win32_ImageList_SetOverlayImage_cpp, commctrl/ImageList_SetOverlayImage, controls.ImageList_SetOverlayImage, controls._win32_ImageList_SetOverlayImage
ms.prod: windows
ms.technology: windows-sdk
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
 - ImageList_SetOverlayImage
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
---

# ImageList_SetOverlayImage function


## -description


Adds a specified image to the list of images to be used as overlay masks. An image list can have up to four overlay masks in version 4.70 and earlier and up to 15 in version 4.71. The function assigns an overlay mask index to the specified image. 


## -parameters




### -param himl [in]

Type: <b>HIMAGELIST</b>

A handle to the image list. 


### -param iImage [in]

Type: <b>int</b>

The zero-based index of an image in the <i>himl</i> image list. This index identifies the image to use as an overlay mask. 


### -param iOverlay [in]

Type: <b>int</b>

The one-based index of the overlay mask. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.




## -remarks



An overlay mask is an image drawn transparently over another image. To draw an overlay mask over an image, call the <a href="https://msdn.microsoft.com/d50d94e4-89cb-4992-b98b-84b22ff11191">ImageList_Draw</a> or <a href="https://msdn.microsoft.com/f531f9b8-a2f5-488b-952b-f439efd83a77">ImageList_DrawEx</a> function. The <i>fStyle</i> parameter of these functions can use the <a href="https://msdn.microsoft.com/6619d390-0c23-41ff-a07b-31425e47712b">INDEXTOOVERLAYMASK</a> macro to specify an overlay mask index. 

A call to this method fails and returns E_INVALIDARG unless the image list is created using a mask.



