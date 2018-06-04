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

# tagPictureAttributes enumeration


## -description


Specifies attributes of a picture object as returned through the <a href="https://msdn.microsoft.com/ed71f0eb-3af4-463f-93e1-29d5dd1cc684">IPicture::get_Attributes</a> method. 


## -enum-fields




### -field PICTURE_SCALABLE

The picture object is scalable, such that it can be redrawn with a different size than was used to create the picture originally. Metafile-based pictures are considered scalable; icon and bitmap pictures, while they can be scaled, do not express this attribute because both involve bitmap stretching instead of true scaling.


### -field PICTURE_TRANSPARENT

The picture object contains an image that has transparent areas, such that drawing the picture will not necessarily fill in all the spaces in the rectangle it occupies. Metafile and icon pictures have this attribute; bitmap pictures do not.


## -see-also




<a href="https://msdn.microsoft.com/ed71f0eb-3af4-463f-93e1-29d5dd1cc684">IPicture::get_Attributes</a>
 

 

