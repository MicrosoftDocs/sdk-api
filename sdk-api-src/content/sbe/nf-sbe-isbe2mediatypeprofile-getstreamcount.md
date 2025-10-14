---
UID: NF:sbe.ISBE2MediaTypeProfile.GetStreamCount
title: ISBE2MediaTypeProfile::GetStreamCount (sbe.h)
description: Gets the number of streams in a media type profile.
helpviewer_keywords: ["GetStreamCount","GetStreamCount method [Microsoft TV Technologies]","GetStreamCount method [Microsoft TV Technologies]","ISBE2MediaTypeProfile interface","ISBE2MediaTypeProfile interface [Microsoft TV Technologies]","GetStreamCount method","ISBE2MediaTypeProfile.GetStreamCount","ISBE2MediaTypeProfile::GetStreamCount","mstv.isbe2mediatypeprofile_getstreamcount","sbe/ISBE2MediaTypeProfile::GetStreamCount"]
old-location: mstv\isbe2mediatypeprofile_getstreamcount.htm
tech.root: mstv
ms.assetid: 9f129ed8-3b61-4291-8400-a5f0905c8b49
ms.date: 12/05/2018
ms.keywords: GetStreamCount, GetStreamCount method [Microsoft TV Technologies], GetStreamCount method [Microsoft TV Technologies],ISBE2MediaTypeProfile interface, ISBE2MediaTypeProfile interface [Microsoft TV Technologies],GetStreamCount method, ISBE2MediaTypeProfile.GetStreamCount, ISBE2MediaTypeProfile::GetStreamCount, mstv.isbe2mediatypeprofile_getstreamcount, sbe/ISBE2MediaTypeProfile::GetStreamCount
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
 - ISBE2MediaTypeProfile::GetStreamCount
 - sbe/ISBE2MediaTypeProfile::GetStreamCount
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
 - ISBE2MediaTypeProfile.GetStreamCount
---

# ISBE2MediaTypeProfile::GetStreamCount


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of streams in a media type profile.

## -parameters

### -param pCount [out]

Receives the number of streams in the profile.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Null pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2mediatypeprofile">ISBE2MediaTypeProfile</a>