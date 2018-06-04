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

# _ASFFlatSynchronisedLyrics structure


## -description



Contains synchronized lyrics stored as metadata for a media source. This structure is used as the data item for the <b>WM/Lyrics_Synchronised</b> metadata attribute.




## -struct-fields




### -field bTimeStampFormat

Specifies the format of time stamps in the lyrics. This member is equivalent to the <b>bTimeStampFormat</b> member in the <b>WM_SYNCHRONISED_LYRICS</b> structure. The <b>WM_SYNCHRONISED_LYRICS</b> structure is documented in the Windows Media Format SDK.


### -field bContentType

Specifies the type of synchronized strings that are in the lyric data. This member is equivalent to the <b>bContentType</b> member in the <b>WM_SYNCHRONISED_LYRICS</b> structure.


### -field dwLyricsLen

Size, in bytes, of the lyric data.


## -remarks



The <b>WM/Lyrics_Synchronised</b> attribute is defined in the Windows Media Format SDK. The attribute contains lyrics synchronized to times in the source file.

To get this attribute from a media source, call <a href="https://msdn.microsoft.com/177c8612-5c9f-4a71-9ee1-a4c67737af2d">IMFMetadata::GetProperty</a>, passing in the constant g_wszWMLyrics_Synchronised for the <i>pwszName</i> parameter. The method retrieves a <b>PROPVARIANT</b> that contains a binary array (VT_BLOB). The layout of the array is as follows:

<ul>
<li>
<b>ASF_FLAT_SYNCHRONISED_LYRICS</b> structure.

</li>
<li>
Null-terminated wide-character string that contains a description.

</li>
<li>
Lyric data. The format of the lyric data is described in the Windows Media Format SDK documentation.

</li>
</ul>
This format differs from the <b>WM_SYNCHRONISED_LYRICS</b> structure used in the Windows Media Format SDK. The <b>WM_SYNCHRONISED_LYRICS</b> structure contains internal pointers to two strings and the lyric data. If the structure is copied, these pointers become invalid. The <b>ASF_FLAT_SYNCHRONISED_LYRICS</b> structure does not contain internal pointers, so it is safe to copy the structure.




## -see-also




<a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

