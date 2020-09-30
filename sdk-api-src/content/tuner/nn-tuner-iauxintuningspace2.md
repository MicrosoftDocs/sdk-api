---
UID: NN:tuner.IAuxInTuningSpace2
title: IAuxInTuningSpace2 (tuner.h)
description: This topic applies to Windows XP Media Center Edition 2004 and later.
helpviewer_keywords: ["IAuxInTuningSpace2","IAuxInTuningSpace2 interface [Microsoft TV Technologies]","IAuxInTuningSpace2 interface [Microsoft TV Technologies]","described","IAuxInTuningSpace2Interface","mstv.iauxintuningspace2","tuner/IAuxInTuningSpace2"]
old-location: mstv\iauxintuningspace2.htm
tech.root: mstv
ms.assetid: 51d92eab-1cf0-451c-aefb-ca36360e29f7
ms.date: 12/05/2018
ms.keywords: IAuxInTuningSpace2, IAuxInTuningSpace2 interface [Microsoft TV Technologies], IAuxInTuningSpace2 interface [Microsoft TV Technologies],described, IAuxInTuningSpace2Interface, mstv.iauxintuningspace2, tuner/IAuxInTuningSpace2
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IAuxInTuningSpace2
 - tuner/IAuxInTuningSpace2
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
 - IAuxInTuningSpace2
---

# IAuxInTuningSpace2 interface


## -description

This topic applies to Windows XP Media Center Edition 2004 and later.
        

The <b>IAuxInTuningSpace2</b> interface is implemented on <a href="/previous-versions/windows/desktop/mstv/auxintuningspace-object">AuxInTuningSpace</a> objects, which represent auxiliary video inputs such as S-video or composite video on a hardware device that is connected to the computer.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAuxInTuningSpace2</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iauxintuningspace~r1">IAuxInTuningSpace</a>. <b>IAuxInTuningSpace2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAuxInTuningSpace2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iauxintuningspace2-get_countrycode">get_CountryCode</a>
</td>
<td align="left" width="63%">
Gets the country/region code of the tuning space (based on TAPI country/region codes).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iauxintuningspace2-put_countrycode">put_CountryCode</a>
</td>
<td align="left" width="63%">
Sets the country/region code of the tuning space (based on TAPI country/region codes).

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAuxInTuningSpace2)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iauxintuningspace~r1">IAuxInTuningSpace</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>