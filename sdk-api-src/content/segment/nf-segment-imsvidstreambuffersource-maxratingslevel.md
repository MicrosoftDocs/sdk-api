---
UID: NF:segment.IMSVidStreamBufferSource.MaxRatingsLevel
title: IMSVidStreamBufferSource::MaxRatingsLevel (segment.h)
author: windows-sdk-content
description: The MaxRatingsLevel method specifies the maximum ratings level the object is permitted to play.
old-location: mstv\imsvidstreambuffersource_maxratingslevel.htm
tech.root: mstv
ms.assetid: 74dbb008-21c9-4651-8386-761626b7bf19
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMSVidStreamBufferSource interface [Microsoft TV Technologies],MaxRatingsLevel method, IMSVidStreamBufferSource.MaxRatingsLevel, IMSVidStreamBufferSource::MaxRatingsLevel, IMSVidStreamBufferSourceMaxRatingsLevel, MaxRatingsLevel, MaxRatingsLevel method [Microsoft TV Technologies], MaxRatingsLevel method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, mstv.imsvidstreambuffersource_maxratingslevel, segment/IMSVidStreamBufferSource::MaxRatingsLevel
ms.topic: method
f1_keywords: ["segment/IMSVidStreamBufferSource.MaxRatingsLevel"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSource.MaxRatingsLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidStreamBufferSource::MaxRatingsLevel


## -description


The <b>MaxRatingsLevel</b> method specifies the maximum ratings level the object is permitted to play.


## -parameters




### -param enSystem [in]

Specifies the rating system, as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-entvrat_system">EnTvRat_System</a> enumeration value.


### -param enRating [in]

Specifies the maximum rating level, as an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-entvrat_genericlevel">EnTvRat_GenericLevel</a> enumeration value.


### -param lbfEnAttr [in]

Specifies zero or more ratings attributes, as a bitwise combination of flags from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tvratings/ne-tvratings-bfentvrat_genericattributes">BfEnTvRat_GenericAttributes</a> enumeration.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidstreambuffersource">IMSVidStreamBufferSource Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tv-ratings-components">TV Ratings Components</a>
 

 

