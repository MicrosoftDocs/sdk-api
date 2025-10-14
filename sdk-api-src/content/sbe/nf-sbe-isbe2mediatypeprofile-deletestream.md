---
UID: NF:sbe.ISBE2MediaTypeProfile.DeleteStream
title: ISBE2MediaTypeProfile::DeleteStream (sbe.h)
description: Removes a stream from a media type profile.
helpviewer_keywords: ["DeleteStream","DeleteStream method [Microsoft TV Technologies]","DeleteStream method [Microsoft TV Technologies]","ISBE2MediaTypeProfile interface","ISBE2MediaTypeProfile interface [Microsoft TV Technologies]","DeleteStream method","ISBE2MediaTypeProfile.DeleteStream","ISBE2MediaTypeProfile::DeleteStream","mstv.isbe2mediatypeprofile_deletestream","sbe/ISBE2MediaTypeProfile::DeleteStream"]
old-location: mstv\isbe2mediatypeprofile_deletestream.htm
tech.root: mstv
ms.assetid: 83e8b802-d28f-4130-addf-772682ac327f
ms.date: 12/05/2018
ms.keywords: DeleteStream, DeleteStream method [Microsoft TV Technologies], DeleteStream method [Microsoft TV Technologies],ISBE2MediaTypeProfile interface, ISBE2MediaTypeProfile interface [Microsoft TV Technologies],DeleteStream method, ISBE2MediaTypeProfile.DeleteStream, ISBE2MediaTypeProfile::DeleteStream, mstv.isbe2mediatypeprofile_deletestream, sbe/ISBE2MediaTypeProfile::DeleteStream
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
 - ISBE2MediaTypeProfile::DeleteStream
 - sbe/ISBE2MediaTypeProfile::DeleteStream
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
 - ISBE2MediaTypeProfile.DeleteStream
---

# ISBE2MediaTypeProfile::DeleteStream


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Removes a stream from a media type  profile.

## -parameters

### -param Index [in]

The index of the stream to remove. To get the number of the streams in the profile, call the <a href="/previous-versions/windows/desktop/api/sbe/nf-sbe-isbe2mediatypeprofile-getstreamcount">ISBE2MediaTypeProfile::GetStreamCount</a> method.

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
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2mediatypeprofile">ISBE2MediaTypeProfile</a>