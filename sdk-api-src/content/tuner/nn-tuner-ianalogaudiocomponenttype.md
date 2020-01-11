---
UID: NN:tuner.IAnalogAudioComponentType
title: IAnalogAudioComponentType (tuner.h)
description: The IAnalogAudioComponentType interface provides methods for accessing the analog audio mode.
old-location: mstv\ianalogaudiocomponenttype.htm
tech.root: mstv
ms.assetid: bd2256b4-6e9a-4520-8988-d271fb2b84af
ms.date: 12/05/2018
ms.keywords: IAnalogAudioComponentType, IAnalogAudioComponentType interface [Microsoft TV Technologies], IAnalogAudioComponentType interface [Microsoft TV Technologies],described, IAnalogAudioComponentTypeInterface, mstv.ianalogaudiocomponenttype, tuner/IAnalogAudioComponentType
f1_keywords:
- tuner/IAnalogAudioComponentType
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tuner.h
api_name:
- IAnalogAudioComponentType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAnalogAudioComponentType interface


## -description



The <b>IAnalogAudioComponentType</b> interface provides methods for accessing the analog audio mode.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAnalogAudioComponentType</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a>. <b>IAnalogAudioComponentType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAnalogAudioComponentType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogaudiocomponenttype-get_analogaudiomode">get_AnalogAudioMode</a>
</td>
<td align="left" width="63%">
Retrieves the analog audio mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ianalogaudiocomponenttype-put_analogaudiomode">put_AnalogAudioMode</a>
</td>
<td align="left" width="63%">
Specifies the analog audio mode.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IAnalogAudioComponentType)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

