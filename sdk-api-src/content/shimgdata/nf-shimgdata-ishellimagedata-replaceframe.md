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

# IShellImageData::ReplaceFrame


## -description


Replaces the current frame with a new image.


## -parameters




### -param pImg [in]

Type: <b>Image*</b>

The address of the new image.


## -returns



Type: <b>HRESULT</b>

Always returns S_OK.




## -remarks



You should also call <a href="https://msdn.microsoft.com/9bd16fa1-530d-46c7-bd1b-4ec9bf596881">IShellImageData::DiscardEdit</a> to ensure that any edited properties of the original image are not retained.

In the case of a multiframed image such as a .gif file, the current frame is replaced. In the case of non-multiframed images such a .jpg file, the entire image is replaced.

Replacing a frame in an animated .gif file causes that file's animation to no longer be functional. Replacing a frame in a Tagged Image File Format (TIFF) file could cause that file to lose pages, particularly if the TIFF frame's image is not the same size as the original. If possible, you should always replace a TIFF frame's image with a TIFF of the same size.

The <a href="https://msdn.microsoft.com/935e651c-4dcd-4317-847e-34adf656035c">IShellImageData</a> implementation takes ownership of the image named in <i>pImg</i> and the caller should not try to use it after calling <b>IShellImageData::ReplaceFrame</b>.



