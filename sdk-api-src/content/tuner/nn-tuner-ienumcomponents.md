---
UID: NN:tuner.IEnumComponents
title: IEnumComponents (tuner.h)
author: windows-sdk-content
description: The IEnumComponents interface provides a standard COM enumeration object for the components (substreams) in a given program stream.
old-location: mstv\ienumcomponents.htm
tech.root: mstv
ms.assetid: 8811021c-8c14-4be6-8802-76b942bb34d8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumComponents, IEnumComponents interface [Microsoft TV Technologies], IEnumComponents interface [Microsoft TV Technologies],described, IEnumComponentsInterface, mstv.ienumcomponents, tuner/IEnumComponents
ms.topic: interface
f1_keywords: 
 - "tuner/IEnumComponents"
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
 - IEnumComponents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumComponents interface


## -description



The <b>IEnumComponents</b> interface provides a standard COM enumeration object for the components (substreams) in a given program stream. C++ applications should use this interface to enumerate components, rather than using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents</a> collection interface, which is intended for Automation clients.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumComponents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumComponents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumComponents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumcomponents-clone">Clone</a>
</td>
<td align="left" width="63%">
Create a new copy of the entire collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumcomponents-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>n</i> elements in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumcomponents-reset">Reset</a>
</td>
<td align="left" width="63%">
Reset the enumerator to the beginning of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumcomponents-skip">Skip</a>
</td>
<td align="left" width="63%">
Skip the specified element in the collection without retrieving it.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumComponents)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

