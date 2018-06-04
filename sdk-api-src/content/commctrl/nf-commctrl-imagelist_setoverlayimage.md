---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



