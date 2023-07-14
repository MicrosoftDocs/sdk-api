---
UID: NF:segment.IMSVidStreamBufferSource.CurrentRatings
title: IMSVidStreamBufferSource::CurrentRatings (segment.h)
description: The CurrentRatings method retrieves the current ratings information from the data source.
helpviewer_keywords: ["CurrentRatings","CurrentRatings method [Microsoft TV Technologies]","CurrentRatings method [Microsoft TV Technologies]","IMSVidStreamBufferSource interface","IMSVidStreamBufferSource interface [Microsoft TV Technologies]","CurrentRatings method","IMSVidStreamBufferSource.CurrentRatings","IMSVidStreamBufferSource::CurrentRatings","IMSVidStreamBufferSourceCurrentRatings","mstv.imsvidstreambuffersource_currentratings","segment/IMSVidStreamBufferSource::CurrentRatings"]
old-location: mstv\imsvidstreambuffersource_currentratings.htm
tech.root: mstv
ms.assetid: c388d972-07d9-4347-97d3-03a46a6bb50c
ms.date: 12/05/2018
ms.keywords: CurrentRatings, CurrentRatings method [Microsoft TV Technologies], CurrentRatings method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, IMSVidStreamBufferSource interface [Microsoft TV Technologies],CurrentRatings method, IMSVidStreamBufferSource.CurrentRatings, IMSVidStreamBufferSource::CurrentRatings, IMSVidStreamBufferSourceCurrentRatings, mstv.imsvidstreambuffersource_currentratings, segment/IMSVidStreamBufferSource::CurrentRatings
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
 - IMSVidStreamBufferSource::CurrentRatings
 - segment/IMSVidStreamBufferSource::CurrentRatings
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
 - IMSVidStreamBufferSource.CurrentRatings
---

# IMSVidStreamBufferSource::CurrentRatings


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>CurrentRatings</b> method retrieves the current ratings information from the data source.

## -parameters

### -param pEnSystem [out]

Pointer to a variable that receives the rating system, as an <a href="/previous-versions/dd375612(v=vs.85)">EnTvRat_System</a> enumeration value.

### -param pEnRating [out]

Receives the rating level, as an <a href="/previous-versions/dd375610(v=vs.85)">EnTvRat_GenericLevel</a> enumeration value.

### -param pBfEnAttr [out]

Pointer to a variable that receives the ratings attributes, as a bitwise combination of zero or more flags from the <a href="/previous-versions/dd318226(v=vs.85)">BfEnTvRat_GenericAttributes</a> enumeration.

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