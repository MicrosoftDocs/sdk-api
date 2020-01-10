---
UID: NN:tuner.IATSCLocator2
title: IATSCLocator2 (tuner.h)
description: The IATASCLocator2 interface enables the network provider to determine the physical channel, transport stream ID, and program number of an ATSC transmission.
old-location: mstv\iatsclocator2.htm
tech.root: mstv
ms.assetid: dbb830bf-db46-4981-8a96-ae33b1de3883
ms.date: 12/05/2018
ms.keywords: IATSCLocator2, IATSCLocator2 interface [Microsoft TV Technologies], IATSCLocator2 interface [Microsoft TV Technologies],described, IATSCLocator2Interface, mstv.iatsclocator2, tuner/IATSCLocator2
f1_keywords:
- tuner/IATSCLocator2
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
- IATSCLocator2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IATSCLocator2 interface


## -description



The <b>IATASCLocator2</b> interface enables the network provider to determine the physical channel, transport stream ID, and program number of an ATSC transmission.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSCLocator2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsclocator">IATSCLocator</a>. <b>IATSCLocator2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSCLocator2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsclocator2-get_programnumber">get_ProgramNumber</a>
</td>
<td align="left" width="63%">
Retrieves the program number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsclocator2-put_programnumber">put_ProgramNumber</a>
</td>
<td align="left" width="63%">
Specifies the program number.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IATSCLocator2)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsclocator">IATSCLocator</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

