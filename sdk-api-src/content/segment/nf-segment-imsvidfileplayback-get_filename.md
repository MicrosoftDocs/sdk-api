---
UID: NF:segment.IMSVidFilePlayback.get_FileName
title: IMSVidFilePlayback::get_FileName (segment.h)
description: The get_FileName method retrieves the name of the file to play.
helpviewer_keywords: ["IMSVidFilePlayback interface [Microsoft TV Technologies]","get_FileName method","IMSVidFilePlayback.get_FileName","IMSVidFilePlayback::get_FileName","IMSVidFilePlaybackget_FileName","get_FileName","get_FileName method [Microsoft TV Technologies]","get_FileName method [Microsoft TV Technologies]","IMSVidFilePlayback interface","mstv.imsvidfileplayback_get_filename","segment/IMSVidFilePlayback::get_FileName"]
old-location: mstv\imsvidfileplayback_get_filename.htm
tech.root: mstv
ms.assetid: c8e01204-fb8e-4ebb-97d9-04dda15c491a
ms.date: 12/05/2018
ms.keywords: IMSVidFilePlayback interface [Microsoft TV Technologies],get_FileName method, IMSVidFilePlayback.get_FileName, IMSVidFilePlayback::get_FileName, IMSVidFilePlaybackget_FileName, get_FileName, get_FileName method [Microsoft TV Technologies], get_FileName method [Microsoft TV Technologies],IMSVidFilePlayback interface, mstv.imsvidfileplayback_get_filename, segment/IMSVidFilePlayback::get_FileName
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidFilePlayback::get_FileName
 - segment/IMSVidFilePlayback::get_FileName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidFilePlayback.get_FileName
---

# IMSVidFilePlayback::get_FileName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_FileName</b> method retrieves the name of the file to play.

## -parameters

### -param FileName [out]

Pointer to a variable that receives the file name.

## -returns

The method returns an <b>HRESULT</b>. Possible values include the following.

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
</table>

## -remarks

The caller must release the returned string, using the <b>CoTaskMemFree</b> function.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidfileplayback">IMSVidFilePlayback Interface</a>