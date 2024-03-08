---
UID: NF:segment.IMSVidStreamBufferSource.MaxRatingsLevel
title: IMSVidStreamBufferSource::MaxRatingsLevel (segment.h)
description: The MaxRatingsLevel method specifies the maximum ratings level the object is permitted to play.
helpviewer_keywords: ["IMSVidStreamBufferSource interface [Microsoft TV Technologies]","MaxRatingsLevel method","IMSVidStreamBufferSource.MaxRatingsLevel","IMSVidStreamBufferSource::MaxRatingsLevel","IMSVidStreamBufferSourceMaxRatingsLevel","MaxRatingsLevel","MaxRatingsLevel method [Microsoft TV Technologies]","MaxRatingsLevel method [Microsoft TV Technologies]","IMSVidStreamBufferSource interface","mstv.imsvidstreambuffersource_maxratingslevel","segment/IMSVidStreamBufferSource::MaxRatingsLevel"]
old-location: mstv\imsvidstreambuffersource_maxratingslevel.htm
tech.root: mstv
ms.assetid: 74dbb008-21c9-4651-8386-761626b7bf19
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSource interface [Microsoft TV Technologies],MaxRatingsLevel method, IMSVidStreamBufferSource.MaxRatingsLevel, IMSVidStreamBufferSource::MaxRatingsLevel, IMSVidStreamBufferSourceMaxRatingsLevel, MaxRatingsLevel, MaxRatingsLevel method [Microsoft TV Technologies], MaxRatingsLevel method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, mstv.imsvidstreambuffersource_maxratingslevel, segment/IMSVidStreamBufferSource::MaxRatingsLevel
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
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
 - IMSVidStreamBufferSource::MaxRatingsLevel
 - segment/IMSVidStreamBufferSource::MaxRatingsLevel
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
 - IMSVidStreamBufferSource.MaxRatingsLevel
---

# IMSVidStreamBufferSource::MaxRatingsLevel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>MaxRatingsLevel</b> method specifies the maximum ratings level the object is permitted to play.

## -parameters

### -param enSystem [in]

Specifies the rating system, as an <a href="/previous-versions/dd375612(v=vs.85)">EnTvRat_System</a> enumeration value.

### -param enRating [in]

Specifies the maximum rating level, as an <a href="/previous-versions/dd375610(v=vs.85)">EnTvRat_GenericLevel</a> enumeration value.

### -param lbfEnAttr [in]

Specifies zero or more ratings attributes, as a bitwise combination of flags from the <a href="/previous-versions/dd318226(v=vs.85)">BfEnTvRat_GenericAttributes</a> enumeration.

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

<a href="/previous-versions/windows/desktop/mstv/msvidstreambuffersource">IMSVidStreamBufferSource Interface</a>



<a href="/previous-versions/windows/desktop/mstv/tv-ratings-components">TV Ratings Components</a>