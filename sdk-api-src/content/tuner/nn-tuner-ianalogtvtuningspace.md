---
UID: NN:tuner.IAnalogTVTuningSpace
title: IAnalogTVTuningSpace (tuner.h)
author: windows-sdk-content
description: The IAnalogTVTuningSpace interface provides methods for getting and setting parameters associated with analog TV tuning spaces. The Video Control uses these methods when building and controlling a WDM Analog TV filter graph.
old-location: mstv\ianalogtvtuningspace.htm
tech.root: mstv
ms.assetid: 2b531f09-bf2e-4eb2-abcf-60f64cbee17b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAnalogTVTuningSpace, IAnalogTVTuningSpace interface [Microsoft TV Technologies], IAnalogTVTuningSpace interface [Microsoft TV Technologies],described, IAnalogTVTuningSpaceInterface, mstv.ianalogtvtuningspace, tuner/IAnalogTVTuningSpace
ms.topic: interface
f1_keywords: ["tuner/IAnalogTVTuningSpace"]
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IAnalogTVTuningSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAnalogTVTuningSpace interface


## -description



The <b>IAnalogTVTuningSpace</b> interface provides methods for getting and setting parameters associated with analog TV tuning spaces. The Video Control uses these methods when building and controlling a WDM Analog TV filter graph.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnalogTVTuningSpace</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a>. <b>IAnalogTVTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnalogTVTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-get_countrycode">get_CountryCode</a>
</td>
<td align="left" width="63%">
Gets the country/region code of the tuning space (based on TAPI country/region codes).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-get_inputtype">get_InputType</a>
</td>
<td align="left" width="63%">
Gets the input type (antenna or cable) intended for the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-get_maxchannel">get_MaxChannel</a>
</td>
<td align="left" width="63%">
Gets the highest channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-get_minchannel">get_MinChannel</a>
</td>
<td align="left" width="63%">
Gets the lowest channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_countrycode">put_CountryCode</a>
</td>
<td align="left" width="63%">
Sets the country/region code of the tuning space (based on TAPI country/region codes).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_inputtype">put_InputType</a>
</td>
<td align="left" width="63%">
Sets the input type (antenna or cable) intended for the tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_maxchannel">put_MaxChannel</a>
</td>
<td align="left" width="63%">
Sets the highest channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_minchannel">put_MinChannel</a>
</td>
<td align="left" width="63%">
Sets the lowest channel number for this tuning space.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAnalogTVTuningSpace)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

