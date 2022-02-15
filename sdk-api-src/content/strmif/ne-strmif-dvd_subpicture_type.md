---
UID: NE:strmif.tagDVD_SUBPICTURE_TYPE
title: DVD_SUBPICTURE_TYPE (strmif.h)
description: Defines flags used to determine what kind of content the subpicture stream contains.
helpviewer_keywords: ["DVD_SPType_Language","DVD_SPType_NotSpecified","DVD_SPType_Other","DVD_SUBPICTURE_TYPE","DVD_SUBPICTURE_TYPE","DVD_SUBPICTURE_TYPE enumeration [DirectShow]","DVD_SUBPICTURE_TYPEEnumeration","dshow.dvd_subpicture_type","strmif/DVD_SPType_Language","strmif/DVD_SPType_NotSpecified","strmif/DVD_SPType_Other","strmif/DVD_SUBPICTURE_TYPE"]
old-location: dshow\dvd_subpicture_type.htm
tech.root: dshow
ms.assetid: c4c5eb83-4773-464d-8b0c-b46b13c3b6d3
ms.date: 12/05/2018
ms.keywords: DVD_SPType_Language, DVD_SPType_NotSpecified, DVD_SPType_Other, DVD_SUBPICTURE_TYPE, DVD_SUBPICTURE_TYPE , DVD_SUBPICTURE_TYPE enumeration [DirectShow], DVD_SUBPICTURE_TYPEEnumeration, dshow.dvd_subpicture_type, strmif/DVD_SPType_Language, strmif/DVD_SPType_NotSpecified, strmif/DVD_SPType_Other, strmif/DVD_SUBPICTURE_TYPE
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
targetos: Windows
req.typenames: DVD_SUBPICTURE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDVD_SUBPICTURE_TYPE
 - strmif/tagDVD_SUBPICTURE_TYPE
 - DVD_SUBPICTURE_TYPE
 - strmif/DVD_SUBPICTURE_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_SUBPICTURE_TYPE
---

# DVD_SUBPICTURE_TYPE enumeration


## -description

Defines flags used to determine what kind of content the subpicture stream contains.

## -enum-fields

### -field DVD_SPType_NotSpecified:0

The DVD does not specify the subpicture type.

### -field DVD_SPType_Language:1

The subpicture contains language-related content such as movie subtitles or other text.

### -field DVD_SPType_Other:2

The subpicture contains nonlanguage-related content such as a bouncing ball in karaoke titles.

## -see-also

[DVD_SubpictureAttributes](/windows/desktop/api/strmif/ns-strmif-dvd_subpictureattributes)



<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
