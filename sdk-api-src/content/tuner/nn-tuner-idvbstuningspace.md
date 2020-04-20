---
UID: NN:tuner.IDVBSTuningSpace
title: IDVBSTuningSpace (tuner.h)
description: The IDVBSTuningSpace interface is implemented on the DVBTuningSpace object and provides methods for working with tuning spaces with a DVBS network type.helpviewer_keywords: ["IDVBSTuningSpace","IDVBSTuningSpace interface [Microsoft TV Technologies]","IDVBSTuningSpace interface [Microsoft TV Technologies]","described","IDVBSTuningSpaceInterface","mstv.idvbstuningspace","tuner/IDVBSTuningSpace"]
old-location: mstv\idvbstuningspace.htm
tech.root: mstv
ms.assetid: 46c143d7-b9ec-4808-a4d2-337e6e0252dd
ms.date: 12/05/2018
ms.keywords: IDVBSTuningSpace, IDVBSTuningSpace interface [Microsoft TV Technologies], IDVBSTuningSpace interface [Microsoft TV Technologies],described, IDVBSTuningSpaceInterface, mstv.idvbstuningspace, tuner/IDVBSTuningSpace
f1_keywords:
- tuner/IDVBSTuningSpace
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
- IDVBSTuningSpace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVBSTuningSpace interface


## -description



The <b>IDVBSTuningSpace</b> interface is implemented on the <b>DVBTuningSpace</b> object and provides methods for working with tuning spaces with a DVBS network type.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDVBSTuningSpace</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtuningspace2">IDVBTuningSpace2</a>. <b>IDVBSTuningSpace</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDVBSTuningSpace</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbstuningspace-get_highoscillator">get_HighOscillator</a>
</td>
<td align="left" width="63%">
Retrieves the high oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbstuningspace-get_inputrange">get_InputRange</a>
</td>
<td align="left" width="63%">
Retrieves an integer indicating which option or switch contains the requested signal source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbstuningspace-get_lnbswitch">get_LNBSwitch</a>
</td>
<td align="left" width="63%">
Retrieves the LNB switch frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbstuningspace-get_lowoscillator">get_LowOscillator</a>
</td>
<td align="left" width="63%">
Retrieves the low oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbstuningspace-get_spectralinversion">get_SpectralInversion</a>
</td>
<td align="left" width="63%">
Retrieves an integer indicating the spectral inversion.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbstuningspace-put_highoscillator">put_HighOscillator</a>
</td>
<td align="left" width="63%">
Sets the high oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbstuningspace-put_inputrange">put_InputRange</a>
</td>
<td align="left" width="63%">
Sets an integer indicating which option or switch contains the requested signal source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbstuningspace-put_lnbswitch">put_LNBSwitch</a>
</td>
<td align="left" width="63%">
Sets the LNB switch frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbstuningspace-put_lowoscillator">put_LowOscillator</a>
</td>
<td align="left" width="63%">
Sets the low oscillator frequency.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-idvbstuningspace-put_spectralinversion">put_SpectralInversion</a>
</td>
<td align="left" width="63%">
Sets an integer indicating the spectral inversion.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IDVBSTuningSpace)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-idvbtuningspace2">IDVBTuningSpace2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

