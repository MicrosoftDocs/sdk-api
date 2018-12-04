---
UID: NF:segment.IMSVidStreamBufferSource.MaxRatingsLevel
title: IMSVidStreamBufferSource::MaxRatingsLevel
author: windows-sdk-content
description: The MaxRatingsLevel method specifies the maximum ratings level the object is permitted to play.
old-location: mstv\imsvidstreambuffersource_maxratingslevel.htm
tech.root: mstv
ms.assetid: 74dbb008-21c9-4651-8386-761626b7bf19
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMSVidStreamBufferSource interface [Microsoft TV Technologies],MaxRatingsLevel method, IMSVidStreamBufferSource.MaxRatingsLevel, IMSVidStreamBufferSource::MaxRatingsLevel, IMSVidStreamBufferSourceMaxRatingsLevel, MaxRatingsLevel, MaxRatingsLevel method [Microsoft TV Technologies], MaxRatingsLevel method [Microsoft TV Technologies],IMSVidStreamBufferSource interface, mstv.imsvidstreambuffersource_maxratingslevel, segment/IMSVidStreamBufferSource::MaxRatingsLevel
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# IMSVidStreamBufferSource::MaxRatingsLevel


## -description


The <b>MaxRatingsLevel</b> method specifies the maximum ratings level the object is permitted to play.


## -parameters




### -param enSystem [in]

Specifies the rating system, as an <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration value.


### -param enRating [in]

Specifies the maximum rating level, as an <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration value.


### -param lbfEnAttr [in]

Specifies zero or more ratings attributes, as a bitwise combination of flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration.


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
 

 

