---
UID: NS:strmif.tagDVD_SubpictureAttributes
title: DVD_SubpictureAttributes (strmif.h)
author: windows-sdk-content
description: The DVD_SubpictureAttributes structure contains information about the DVD subpicture. The IDvdInfo2::GetSubpictureAttributes method fills in a DVD_SubpictureAttributes structure for a specified stream.
old-location: dshow\dvd_subpictureattributes.htm
tech.root: DirectShow
ms.assetid: 55ddfa21-5600-4aa9-b554-7ff7f3c05b91
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DVD_SubpictureAttributes, DVD_SubpictureAttributes structure [DirectShow], DVD_SubpictureAttributesStructure, dshow.dvd_subpictureattributes, strmif/DVD_SubpictureAttributes
ms.topic: struct
f1_keywords: 
 - "strmif/DVD_SubpictureAttributes"
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
 - DVD_SubpictureAttributes
product: Windows
targetos: Windows
req.typenames: DVD_SubpictureAttributes
req.redist: 
ms.custom: 19H1
---

# DVD_SubpictureAttributes structure


## -description



The <code>DVD_SubpictureAttributes</code> structure contains information about the DVD subpicture. The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getsubpictureattributes">IDvdInfo2::GetSubpictureAttributes</a> method fills in a <code>DVD_SubpictureAttributes</code> structure for a specified stream.




## -struct-fields




### -field Type

Variable of type <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagdvd_subpicture_type">DVD_SUBPICTURE_TYPE</a> that indicates whether the subpicture contains language-related content.


### -field CodingMode

Variable of type <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagdvd_subpicture_coding">DVD_SUBPICTURE_CODING</a> that indicates how the subpicture graphics stream is encoded.


### -field Language

Variable of type LCID that identifies the subpicture language if Type equals DVD_SPType_Language.


### -field LanguageExtension

Variable of type <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagdvd_subpicture_lang_ext">DVD_SUBPICTURE_LANG_EXT</a> that identifies the subpicture language extension if Type equals DVD_SPType_Language.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>
 

 

