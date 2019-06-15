---
UID: NN:tuner.IAnalogRadioTuningSpace
title: IAnalogRadioTuningSpace (tuner.h)
author: windows-sdk-content
description: The IAnalogRadioTuningSpace interface provides methods for getting and setting parameters associated with tuning spaces for analog radio transmissions.
old-location: mstv\ianalogradiotuningspace.htm
tech.root: mstv
ms.assetid: 25cf9f31-88a9-479e-b51c-ad823cd04d2d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAnalogRadioTuningSpace, IAnalogRadioTuningSpace interface [Microsoft TV Technologies], IAnalogRadioTuningSpace interface [Microsoft TV Technologies],described, IAnalogRadioTuningSpaceInterface, mstv.ianalogradiotuningspace, tuner/IAnalogRadioTuningSpace
ms.topic: interface
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
 - IAnalogRadioTuningSpace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAnalogRadioTuningSpace interface


## -description



The <b>IAnalogRadioTuningSpace</b> interface provides methods for getting and setting parameters associated with tuning spaces for analog radio transmissions.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnalogRadioTuningSpace</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a>. <b>IAnalogRadioTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnalogRadioTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogradiotuningspace-get_maxfrequency">get_MaxFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the maximum frequency for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogradiotuningspace-get_minfrequency">get_MinFrequency</a>
</td>
<td align="left" width="63%">
Retrieves the minimum frequency for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogradiotuningspace-get_step">get_Step</a>
</td>
<td align="left" width="63%">
Retrieves the step increment for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogradiotuningspace-put_maxfrequency">put_MaxFrequency</a>
</td>
<td align="left" width="63%">
Sets the maximum frequency for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogradiotuningspace-put_minfrequency">put_MinFrequency</a>
</td>
<td align="left" width="63%">
Sets the minimum frequency for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogradiotuningspace-put_step">put_Step</a>
</td>
<td align="left" width="63%">
Sets the step increment for this tuning space.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAnalogRadioTuningSpace)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

