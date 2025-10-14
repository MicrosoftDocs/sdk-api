---
UID: NF:sbe.ISBE2MediaTypeProfile.GetStream
title: ISBE2MediaTypeProfile::GetStream (sbe.h)
description: Gets the media type of a stream that appears at a specific index in a media type profile.
helpviewer_keywords: ["GetStream","GetStream method [Microsoft TV Technologies]","GetStream method [Microsoft TV Technologies]","ISBE2MediaTypeProfile interface","ISBE2MediaTypeProfile interface [Microsoft TV Technologies]","GetStream method","ISBE2MediaTypeProfile.GetStream","ISBE2MediaTypeProfile::GetStream","mstv.isbe2mediatypeprofile_getstream","sbe/ISBE2MediaTypeProfile::GetStream"]
old-location: mstv\isbe2mediatypeprofile_getstream.htm
tech.root: mstv
ms.assetid: 14c48484-59b0-4e39-8684-9875edfd6556
ms.date: 12/05/2018
ms.keywords: GetStream, GetStream method [Microsoft TV Technologies], GetStream method [Microsoft TV Technologies],ISBE2MediaTypeProfile interface, ISBE2MediaTypeProfile interface [Microsoft TV Technologies],GetStream method, ISBE2MediaTypeProfile.GetStream, ISBE2MediaTypeProfile::GetStream, mstv.isbe2mediatypeprofile_getstream, sbe/ISBE2MediaTypeProfile::GetStream
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows�7 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISBE2MediaTypeProfile::GetStream
 - sbe/ISBE2MediaTypeProfile::GetStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbe.dll
api_name:
 - ISBE2MediaTypeProfile.GetStream
---

# ISBE2MediaTypeProfile::GetStream


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the media type of a stream that appears at a specific index in a media type  profile.

## -parameters

### -param Index [in]

The index of the stream. To get the number of the streams in the profile, call the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2mediatypeprofile-getstreamcount">ISBE2MediaTypeProfile::GetStreamCount</a> method.

### -param ppMediaType [out]

Receives a pointer to an <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure. The caller must not modify this structure or release the memory allocated for it.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory for media type pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Null media type pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2mediatypeprofile">ISBE2MediaTypeProfile</a>