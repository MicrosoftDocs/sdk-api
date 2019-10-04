---
UID: NN:tuner.IATSCTuningSpace
title: IATSCTuningSpace (tuner.h)
author: windows-sdk-content
description: The IATSCTuningSpace interface is implemented on ATSCTuningSpace objects, which represent any tuning space with an ATSC network type.
old-location: mstv\iatsctuningspace.htm
tech.root: mstv
ms.assetid: 313508e5-a9b2-42b8-bb2f-d191944d0939
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IATSCTuningSpace, IATSCTuningSpace interface [Microsoft TV Technologies], IATSCTuningSpace interface [Microsoft TV Technologies],described, IATSCTuningSpaceInterface, mstv.iatsctuningspace, tuner/IATSCTuningSpace
ms.topic: interface
f1_keywords: 
 - "tuner/IATSCTuningSpace"
dev_langs:
 - c++
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
 - IATSCTuningSpace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IATSCTuningSpace interface


## -description



The <b>IATSCTuningSpace</b> interface is implemented on <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/atsctuningspace-object">ATSCTuningSpace</a> objects, which represent any tuning space with an ATSC network type. Microsoft provides a default ATSC tuning space with Windows XP, and also with DirectX 9.0. Third parties such as cable providers may install a custom tuning space using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer</a> interface. An ATSCTuningSpace object creates tune requests that expose <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iatscchanneltunerequest">IATSCChannelTuneRequest</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSCTuningSpace</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace</a>. <b>IATSCTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSCTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-get_maxminorchannel">get_MaxMinorChannel</a>
</td>
<td align="left" width="63%">
Gets the highest minor channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-get_maxphysicalchannel">get_MaxPhysicalChannel</a>
</td>
<td align="left" width="63%">
Gets the highest physical channel number ever allowed for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-get_minminorchannel">get_MinMinorChannel</a>
</td>
<td align="left" width="63%">
Gets the lowest minor channel number ever allowed for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-get_minphysicalchannel">get_MinPhysicalChannel</a>
</td>
<td align="left" width="63%">
Gets the lowest physical channel number ever allowed for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-put_maxminorchannel">put_MaxMinorChannel</a>
</td>
<td align="left" width="63%">
Sets the highest minor channel number for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-put_maxphysicalchannel">put_MaxPhysicalChannel</a>
</td>
<td align="left" width="63%">
Sets the highest physical channel number ever allowed for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-put_minminorchannel">put_MinMinorChannel</a>
</td>
<td align="left" width="63%">
Sets the lowest minor channel number ever allowed for this tuning space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsctuningspace-put_minphysicalchannel">put_MinPhysicalChannel</a>
</td>
<td align="left" width="63%">
Sets the lowest physical channel number ever allowed for this tuning space.

</td>
</tr>
</table> 


## -remarks



If the minimum and maximum channels are set, and the user specifies a channel that is greater than the maximum, the tuner automatically wraps around to the minimum value.

To set the minimum and maximum major channel, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_minchannel">IAnalogTVTuningSpace::put_MinChannel</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogtvtuningspace-put_maxchannel">IAnalogTVTuningSpace::put_MaxChannel</a>.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCTuningSpace)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ianalogtvtuningspace">IAnalogTVTuningSpace</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

