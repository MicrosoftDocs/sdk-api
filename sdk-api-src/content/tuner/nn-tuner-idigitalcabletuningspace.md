---
UID: NN:tuner.IDigitalCableTuningSpace
title: IDigitalCableTuningSpace (tuner.h)
description: The IDigitalCableTuningSpace interface is implemented on the DigitalTuningSpace object and provides methods for working with tuning spaces that have a digital cable network type.
helpviewer_keywords: ["IDigitalCableTuningSpace","IDigitalCableTuningSpace interface [Microsoft TV Technologies]","IDigitalCableTuningSpace interface [Microsoft TV Technologies]","described","IDigitalCableTuningSpaceInterface","mstv.idigitalcabletuningspace","tuner/IDigitalCableTuningSpace"]
old-location: mstv\idigitalcabletuningspace.htm
tech.root: mstv
ms.assetid: a0788405-5502-4d6a-8f94-9957859ac1af
ms.date: 12/05/2018
ms.keywords: IDigitalCableTuningSpace, IDigitalCableTuningSpace interface [Microsoft TV Technologies], IDigitalCableTuningSpace interface [Microsoft TV Technologies],described, IDigitalCableTuningSpaceInterface, mstv.idigitalcabletuningspace, tuner/IDigitalCableTuningSpace
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDigitalCableTuningSpace
 - tuner/IDigitalCableTuningSpace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IDigitalCableTuningSpace
---

# IDigitalCableTuningSpace interface


## -description

The <b>IDigitalCableTuningSpace</b> interface is implemented on the DigitalTuningSpace object and provides methods for working with tuning spaces that have a digital cable network type.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDigitalCableTuningSpace</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace</a>. <b>IDigitalCableTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDigitalCableTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idigitalcabletuningspace-get_maxmajorchannel">get_MaxMajorChannel</a>
</td>
<td align="left" width="63%">
Retrieves the highest major channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idigitalcabletuningspace-get_maxsourceid">get_MaxSourceID</a>
</td>
<td align="left" width="63%">
Retrieves the highest source identifier for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idigitalcabletuningspace-get_minmajorchannel">get_MinMajorChannel</a>
</td>
<td align="left" width="63%">
Retrieves the lowest major channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idigitalcabletuningspace-get_minsourceid">get_MinSourceID</a>
</td>
<td align="left" width="63%">
Retrieves the lowest source identifier for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idigitalcabletuningspace-put_maxmajorchannel">put_MaxMajorChannel</a>
</td>
<td align="left" width="63%">
Sets the highest major channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idigitalcabletuningspace-put_maxsourceid">put_MaxSourceID</a>
</td>
<td align="left" width="63%">
Sets the highest source identifier for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idigitalcabletuningspace-put_minmajorchannel">put_MinMajorChannel</a>
</td>
<td align="left" width="63%">
Sets the lowest major channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idigitalcabletuningspace-put_minsourceid">put_MinSourceID</a>
</td>
<td align="left" width="63%">
Sets the lowest source identifier for this tuning space.

</td>
</tr>
</table>

## -remarks

To set minimum and maximum values for the virtual channel number, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_minchannel">IAnalogTVTuningSpace::put_MinChannel</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_maxchannel">IAnalogTVTuningSpace::put_MaxChannel</a> methods. (This interface inherits <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace</a> through <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace</a>.)
      

To set minimum and maximum values for the minor channel number, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-put_minminorchannel">IATSCTuningSpace::put_MinMinorChannel</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-put_maxminorchannel">IATSCTuningSpace::put_MaxMinorChannel</a> methods.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDigitalCableTuningSpace)</code>.

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsctuningspace">IATSCTuningSpace</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>

