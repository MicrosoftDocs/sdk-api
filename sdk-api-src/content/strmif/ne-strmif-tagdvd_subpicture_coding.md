---
UID: NE:strmif.tagDVD_SUBPICTURE_CODING
title: tagDVD_SUBPICTURE_CODING
author: windows-sdk-content
description: Indicates what kind of content the subpicture stream contains.
old-location: dshow\dvd_subpicture_coding.htm
tech.root: DirectShow
ms.assetid: 46f45dfb-9be7-4222-b6fb-ea95b60323cd
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DVD_SPCoding_Extended, DVD_SPCoding_Other, DVD_SPCoding_RunLength, DVD_SUBPICTURE_CODING, DVD_SUBPICTURE_CODING , DVD_SUBPICTURE_CODING enumeration [DirectShow], DVD_SUBPICTURE_CODINGEnumeration, dshow.dvd_subpicture_coding, strmif/DVD_SPCoding_Extended, strmif/DVD_SPCoding_Other, strmif/DVD_SPCoding_RunLength, strmif/DVD_SUBPICTURE_CODING, tagDVD_SUBPICTURE_CODING
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_SUBPICTURE_CODING
product: Windows
targetos: Windows
req.typenames: DVD_SUBPICTURE_CODING
req.redist: 
---

# tagDVD_SUBPICTURE_CODING enumeration


## -description



Indicates what kind of content the subpicture stream contains.




## -enum-fields




### -field DVD_SPCoding_RunLength

Indicates that the subpicture uses run length encoding.
          


### -field DVD_SPCoding_Extended

Indicates that subpicture uses extended encoding.
          


### -field DVD_SPCoding_Other

Indicates that the subpicture uses some other encoding scheme.
          


## -remarks



Most subpicture streams contain language-related content such as movie subtitles, but subpictures can also be used for the bouncing ball in karaoke or other non-language-related purposes.




## -see-also




<a href="https://msdn.microsoft.com/55ddfa21-5600-4aa9-b554-7ff7f3c05b91">DVD_SubpictureAttributes</a>



<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

