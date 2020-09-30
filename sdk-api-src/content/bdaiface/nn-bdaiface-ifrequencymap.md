---
UID: NN:bdaiface.IFrequencyMap
title: IFrequencyMap (bdaiface.h)
description: The IFrequencyMap interface sets the frequency table used by the BDA Network Provider filter.A frequency table is a list of broadcast or cable frequencies for a given country/region.
helpviewer_keywords: ["IFrequencyMap","IFrequencyMap interface [Microsoft TV Technologies]","IFrequencyMap interface [Microsoft TV Technologies]","described","IFrequencyMapInterface","bdaiface/IFrequencyMap","mstv.ifrequencymap"]
old-location: mstv\ifrequencymap.htm
tech.root: mstv
ms.assetid: 0f7f1b2c-a191-45f5-a645-367e898b6ee2
ms.date: 12/05/2018
ms.keywords: IFrequencyMap, IFrequencyMap interface [Microsoft TV Technologies], IFrequencyMap interface [Microsoft TV Technologies],described, IFrequencyMapInterface, bdaiface/IFrequencyMap, mstv.ifrequencymap
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IFrequencyMap
 - bdaiface/IFrequencyMap
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IFrequencyMap
---

# IFrequencyMap interface


## -description

The <b>IFrequencyMap</b> interface sets the frequency table used by the <a href="/previous-versions/windows/desktop/mstv/bda-network-provider-filter">BDA Network Provider</a> filter.

A frequency table is a list of broadcast or cable frequencies for a given country/region. The Network Provider uses a frequency table to find the next frequency when <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iscanningtuner">IScanningTuner</a> methods are called. On startup, the Network Provider loads a default frequency table. An application can use the <b>IFrequencyMap</b> interface to specify the user's country/region, which causes the Network Provider filter to load the corresponding frequency table. The application can also modify the current table, or provide a completely new table, using the <a href="/windows/desktop/api/bdaiface/nf-bdaiface-ifrequencymap-put_frequencymapping">put_FrequencyMapping</a> method.

Frequencies used by this interface are measured in units of kilohertz (kHz), and refer to the center frequency of each band. For more information, see "Terrestrial delivery system descriptor" in the ETSI EN 300 468 standard.

<div class="alert"><b>Note</b>  Currently only the DVB-T Network Provider supports this interface.</div>
<div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFrequencyMap</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IFrequencyMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFrequencyMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ifrequencymap-get_countrycode">get_CountryCode</a>
</td>
<td align="left" width="63%">
Returns the country/region code that the Network Provider is currently using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ifrequencymap-get_countrycodelist">get_CountryCodeList</a>
</td>
<td align="left" width="63%">
Returns a list of all the country/region codes for which the Network Provider has a frequency table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ifrequencymap-get_defaultfrequencymapping">get_DefaultFrequencyMapping</a>
</td>
<td align="left" width="63%">
Returns the default frequency table for a given country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ifrequencymap-get_frequencymapping">get_FrequencyMapping</a>
</td>
<td align="left" width="63%">
Returns the Network Provider filter's current frequency table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ifrequencymap-put_countrycode">put_CountryCode</a>
</td>
<td align="left" width="63%">
Sets the country/region code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/bdaiface/nf-bdaiface-ifrequencymap-put_frequencymapping">put_FrequencyMapping</a>
</td>
<td align="left" width="63%">
Sets the frequency table.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IFrequencyMap)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>