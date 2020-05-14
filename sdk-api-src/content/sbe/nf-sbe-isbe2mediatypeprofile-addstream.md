---
UID: NF:sbe.ISBE2MediaTypeProfile.AddStream
title: ISBE2MediaTypeProfile::AddStream (sbe.h)
description: Adds a stream to a media type profile.helpviewer_keywords: ["AddStream","AddStream method [Microsoft TV Technologies]","AddStream method [Microsoft TV Technologies]","ISBE2MediaTypeProfile interface","ISBE2MediaTypeProfile interface [Microsoft TV Technologies]","AddStream method","ISBE2MediaTypeProfile.AddStream","ISBE2MediaTypeProfile::AddStream","mstv.isbe2mediatypeprofile_addstream","sbe/ISBE2MediaTypeProfile::AddStream"]
old-location: mstv\isbe2mediatypeprofile_addstream.htm
tech.root: mstv
ms.assetid: f847d4f1-e748-4ed5-bc79-cfff90601379
ms.date: 12/05/2018
ms.keywords: AddStream, AddStream method [Microsoft TV Technologies], AddStream method [Microsoft TV Technologies],ISBE2MediaTypeProfile interface, ISBE2MediaTypeProfile interface [Microsoft TV Technologies],AddStream method, ISBE2MediaTypeProfile.AddStream, ISBE2MediaTypeProfile::AddStream, mstv.isbe2mediatypeprofile_addstream, sbe/ISBE2MediaTypeProfile::AddStream
f1_keywords:
- sbe/ISBE2MediaTypeProfile.AddStream
dev_langs:
- c++
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Sbe.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sbe.dll
api_name:
- ISBE2MediaTypeProfile.AddStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISBE2MediaTypeProfile::AddStream


## -description


Adds a stream to a media type profile.


## -parameters




### -param pMediaType [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure that specifies the media type of the stream that is added to the profile.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2mediatypeprofile">ISBE2MediaTypeProfile</a>
 

 

