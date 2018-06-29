---
UID: NF:segment.IMSVidStreamBufferSource.CurrentRatings
title: IMSVidStreamBufferSource::CurrentRatings
author: windows-sdk-content
description: The CurrentRatings method retrieves the current ratings information from the data source.
old-location: mstv\imsvidstreambuffersource_currentratings.htm
old-project: mstv
ms.assetid: c388d972-07d9-4347-97d3-03a46a6bb50c
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: CurrentRatings, CurrentRatings method [Microsoft TV Technologies], CurrentRatings method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, IMSVidStreamBufferSource interface [Microsoft TV Technologies],CurrentRatings method, IMSVidStreamBufferSource.CurrentRatings, IMSVidStreamBufferSource::CurrentRatings, IMSVidStreamBufferSourceCurrentRatings, mstv.imsvidstreambuffersource_currentratings, segment/IMSVidStreamBufferSource::CurrentRatings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: SourceSizeList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSource.CurrentRatings
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IMSVidStreamBufferSource::CurrentRatings


## -description


The <b>CurrentRatings</b> method retrieves the current ratings information from the data source.


## -parameters




### -param pEnSystem [out]

Pointer to a variable that receives the rating system, as an <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration value.


### -param pEnRating [out]

Receives the rating level, as an <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration value.
          


### -param pBfEnAttr [out]

Pointer to a variable that receives the ratings attributes, as a bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration.


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




<a href="https://msdn.microsoft.com/12160959-820b-4534-9392-a13ad229317d">IMSVidStreamBufferSource Interface</a>



<a href="https://msdn.microsoft.com/3c17dab4-9ee9-4c7e-bbe0-2f4c5782c015">TV Ratings Components</a>
 

 

