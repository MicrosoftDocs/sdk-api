---
UID: NN:tuner.IEnumTuningSpaces
title: IEnumTuningSpaces (tuner.h)
author: windows-sdk-content
description: The IEnumTuningSpaces interface is implemented on a standard COM collection of tuning space objects and is obtained through various ITuningSpaceContainer.
old-location: mstv\ienumtuningspaces.htm
tech.root: mstv
ms.assetid: 9b64a48f-ebab-46af-a89d-b8bc488d85da
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumTuningSpaces, IEnumTuningSpaces interface [Microsoft TV Technologies], IEnumTuningSpaces interface [Microsoft TV Technologies],described, IEnumTuningSpacesInterface, mstv.ienumtuningspaces, tuner/IEnumTuningSpaces
ms.topic: interface
f1_keywords: 
 - "tuner/IEnumTuningSpaces"
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
 - IEnumTuningSpaces
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumTuningSpaces interface


## -description



The <b>IEnumTuningSpaces</b> interface is implemented on a standard COM collection of tuning space objects and is obtained through various <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTuningSpaces</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumTuningSpaces</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTuningSpaces</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumtuningspaces-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the collection and all its sub-objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumtuningspaces-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>n</i> element in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumtuningspaces-reset">Reset</a>
</td>
<td align="left" width="63%">
Moves the iterator to the beginning of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ienumtuningspaces-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified element in the collection.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumTuningSpaces)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

