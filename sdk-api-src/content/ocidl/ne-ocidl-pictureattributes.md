---
UID: NE:ocidl.tagPictureAttributes
title: PICTUREATTRIBUTES (ocidl.h)
author: windows-sdk-content
description: Specifies attributes of a picture object as returned through the IPicture::get_Attributes method.
old-location: com\pictureattributes.htm
tech.root: com
ms.assetid: 3162a305-d35c-402d-a8d8-f0f124257dd5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PICTUREATTRIBUTES, PICTUREATTRIBUTES enumeration [COM], PICTURE_SCALABLE, PICTURE_TRANSPARENT, _ctrl_PICTURE, com.pictureattributes, ocidl/PICTUREATTRIBUTES, ocidl/PICTURE_SCALABLE, ocidl/PICTURE_TRANSPARENT
ms.topic: enum
f1_keywords: 
 - "ocidl/PICTUREATTRIBUTES"
dev_langs:
 - c++
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - OCIdl.h
api_name:
 - PICTUREATTRIBUTES
targetos: Windows
req.typenames: PICTUREATTRIBUTES
req.redist: 
ms.custom: 19H1
---

# PICTUREATTRIBUTES enumeration


## -description


Specifies attributes of a picture object as returned through the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_attributes">IPicture::get_Attributes</a> method. 


## -enum-fields




### -field PICTURE_SCALABLE

The picture object is scalable, such that it can be redrawn with a different size than was used to create the picture originally. Metafile-based pictures are considered scalable; icon and bitmap pictures, while they can be scaled, do not express this attribute because both involve bitmap stretching instead of true scaling.


### -field PICTURE_TRANSPARENT

The picture object contains an image that has transparent areas, such that drawing the picture will not necessarily fill in all the spaces in the rectangle it occupies. Metafile and icon pictures have this attribute; bitmap pictures do not.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipicture-get_attributes">IPicture::get_Attributes</a>
 

 

