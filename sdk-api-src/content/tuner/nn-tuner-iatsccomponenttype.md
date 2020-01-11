---
UID: NN:tuner.IATSCComponentType
title: IATSCComponentType (tuner.h)
description: The IATSCComponentType interface represents a component type for a component in an ATSC broadcast. The ATSCComponentType object exposes this interface. Use this interface to determine if an audio stream is in AC-3 format.
old-location: mstv\iatsccomponenttype.htm
tech.root: mstv
ms.assetid: c7e05f63-b2cf-4a99-8e0f-bc7ec00463cf
ms.date: 12/05/2018
ms.keywords: IATSCComponentType, IATSCComponentType interface [Microsoft TV Technologies], IATSCComponentType interface [Microsoft TV Technologies],described, IATSCComponentTypeInterface, mstv.iatsccomponenttype, tuner/IATSCComponentType
f1_keywords:
- tuner/IATSCComponentType
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
- IATSCComponentType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IATSCComponentType interface


## -description



The <b>IATSCComponentType</b> interface represents a component type for a component in an ATSC broadcast. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/atsccomponenttype-object">ATSCComponentType</a> object exposes this interface. Use this interface to determine if an audio stream is in AC-3 format.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSCComponentType</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2componenttype">IMPEG2ComponentType</a>. <b>IATSCComponentType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSCComponentType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsccomponenttype-get_flags">get_Flags</a>
</td>
<td align="left" width="63%">
Queries whether an audio component is in AC-3 format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsccomponenttype-put_flags">put_Flags</a>
</td>
<td align="left" width="63%">
Specifies whether an audio component is in AC-3 format.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCComponentType)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2componenttype">IMPEG2ComponentType</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

