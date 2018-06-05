---
UID: NS:strmif.tagDVD_SubpictureAttributes
title: tagDVD_SubpictureAttributes
author: windows-sdk-content
description: The DVD_SubpictureAttributes structure contains information about the DVD subpicture. The IDvdInfo2::GetSubpictureAttributes method fills in a DVD_SubpictureAttributes structure for a specified stream.
old-location: dshow\dvd_subpictureattributes.htm
old-project: DirectShow
ms.assetid: 55ddfa21-5600-4aa9-b554-7ff7f3c05b91
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DVD_SubpictureAttributes, DVD_SubpictureAttributes structure [DirectShow], DVD_SubpictureAttributesStructure, dshow.dvd_subpictureattributes, strmif/DVD_SubpictureAttributes, tagDVD_SubpictureAttributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: DVD_SubpictureAttributes
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	strmif.h
api_name:
-	DVD_SubpictureAttributes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# tagDVD_SubpictureAttributes structure


## -description



The <code>DVD_SubpictureAttributes</code> structure contains information about the DVD subpicture. The <a href="https://msdn.microsoft.com/3dce0c01-1d39-4f49-984b-8cce08a2e67b">IDvdInfo2::GetSubpictureAttributes</a> method fills in a <code>DVD_SubpictureAttributes</code> structure for a specified stream.




## -struct-fields




### -field Type

Variable of type <a href="https://msdn.microsoft.com/c4c5eb83-4773-464d-8b0c-b46b13c3b6d3">DVD_SUBPICTURE_TYPE</a> that indicates whether the subpicture contains language-related content.


### -field CodingMode

Variable of type <a href="https://msdn.microsoft.com/46f45dfb-9be7-4222-b6fb-ea95b60323cd">DVD_SUBPICTURE_CODING</a> that indicates how the subpicture graphics stream is encoded.


### -field Language

Variable of type LCID that identifies the subpicture language if Type equals DVD_SPType_Language.


### -field LanguageExtension

Variable of type <a href="https://msdn.microsoft.com/314c6187-a475-44c9-b22a-b168211fceb3">DVD_SUBPICTURE_LANG_EXT</a> that identifies the subpicture language extension if Type equals DVD_SPType_Language.


## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

