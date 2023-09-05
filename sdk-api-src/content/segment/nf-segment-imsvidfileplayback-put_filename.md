---
UID: NF:segment.IMSVidFilePlayback.put_FileName
title: IMSVidFilePlayback::put_FileName (segment.h)
description: The put_FileName method sets the name of the file to play.
helpviewer_keywords: ["IMSVidFilePlayback interface [Microsoft TV Technologies]","put_FileName method","IMSVidFilePlayback.put_FileName","IMSVidFilePlayback::put_FileName","IMSVidFilePlaybackput_FileName","mstv.imsvidfileplayback_put_filename","put_FileName","put_FileName method [Microsoft TV Technologies]","put_FileName method [Microsoft TV Technologies]","IMSVidFilePlayback interface","segment/IMSVidFilePlayback::put_FileName"]
old-location: mstv\imsvidfileplayback_put_filename.htm
tech.root: mstv
ms.assetid: 1055a053-28d3-470f-aff5-ade71eebc809
ms.date: 12/05/2018
ms.keywords: IMSVidFilePlayback interface [Microsoft TV Technologies],put_FileName method, IMSVidFilePlayback.put_FileName, IMSVidFilePlayback::put_FileName, IMSVidFilePlaybackput_FileName, mstv.imsvidfileplayback_put_filename, put_FileName, put_FileName method [Microsoft TV Technologies], put_FileName method [Microsoft TV Technologies],IMSVidFilePlayback interface, segment/IMSVidFilePlayback::put_FileName
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
 - IMSVidFilePlayback::put_FileName
 - segment/IMSVidFilePlayback::put_FileName
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
 - IMSVidFilePlayback.put_FileName
---

# IMSVidFilePlayback::put_FileName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_FileName</b> method sets the name of the file to play.

## -parameters

### -param FileName [in]

Specifies the file name.

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

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidfileplayback">IMSVidFilePlayback Interface</a>