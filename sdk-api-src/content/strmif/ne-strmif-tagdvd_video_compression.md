---
UID: NE:strmif.tagDVD_VIDEO_COMPRESSION
title: tagDVD_VIDEO_COMPRESSION
author: windows-sdk-content
description: Defines the possible DVD video compression types.
old-location: dshow\dvd_video_compression.htm
old-project: DirectShow
ms.assetid: e147a860-4c69-4da0-96d1-dfc4957880d9
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: DVD_VIDEO_COMPRESSION, DVD_VIDEO_COMPRESSION , DVD_VIDEO_COMPRESSION enumeration [DirectShow], DVD_VIDEO_COMPRESSIONEnumeration, DVD_VideoCompression_MPEG1, DVD_VideoCompression_MPEG2, DVD_VideoCompression_Other, dshow.dvd_video_compression, strmif/DVD_VIDEO_COMPRESSION, strmif/DVD_VideoCompression_MPEG1, strmif/DVD_VideoCompression_MPEG2, strmif/DVD_VideoCompression_Other, tagDVD_VIDEO_COMPRESSION
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
tech.root: 
req.typenames: DVD_VIDEO_COMPRESSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_VIDEO_COMPRESSION
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# tagDVD_VIDEO_COMPRESSION enumeration


## -description



Defines the possible DVD video compression types.




## -enum-fields




### -field DVD_VideoCompression_Other

Unrecognized compression type.
          


### -field DVD_VideoCompression_MPEG1

MPEG-1 compression type.
          


### -field DVD_VideoCompression_MPEG2

MPEG-2 compression type.
          


## -remarks



This enumeration is a member of the <a href="https://msdn.microsoft.com/b395a322-d63e-41a0-b97a-88f99aeba0e5">DVD_VideoAttributes</a> structure, which is filled by a call to the <a href="https://msdn.microsoft.com/92bd3af9-7057-4bf7-9026-d4862c271a03">IDvdInfo2::GetCurrentVideoAttributes</a> method.




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

