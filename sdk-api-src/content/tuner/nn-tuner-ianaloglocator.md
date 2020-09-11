---
UID: NN:tuner.IAnalogLocator
title: IAnalogLocator (tuner.h)
description: The IAnalogLocator interface provides tuning information for an analog television network.
helpviewer_keywords: ["IAnalogLocator","IAnalogLocator interface [Microsoft TV Technologies]","IAnalogLocator interface [Microsoft TV Technologies]","described","IAnalogLocatorInterface","mstv.ianaloglocator","tuner/IAnalogLocator"]
old-location: mstv\ianaloglocator.htm
tech.root: mstv
ms.assetid: d5ed0dcc-347d-4196-a551-88775cb1b253
ms.date: 12/05/2018
ms.keywords: IAnalogLocator, IAnalogLocator interface [Microsoft TV Technologies], IAnalogLocator interface [Microsoft TV Technologies],described, IAnalogLocatorInterface, mstv.ianaloglocator, tuner/IAnalogLocator
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
 - IAnalogLocator
 - tuner/IAnalogLocator
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
 - IAnalogLocator
---

# IAnalogLocator interface


## -description

The <b>IAnalogLocator</b> interface provides tuning information for an analog television network.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnalogLocator</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>. <b>IAnalogLocator</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnalogLocator</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianaloglocator-get_videostandard">get_VideoStandard</a>
</td>
<td align="left" width="63%">
Retrieves the format of the analog television signal.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianaloglocator-put_videostandard">put_VideoStandard</a>
</td>
<td align="left" width="63%">
Specifies the format of the analog television signal.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAnalogLocator)</code>.

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ilocator">ILocator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>

