---
UID: NN:tuner.ITuningSpaces
title: ITuningSpaces (tuner.h)
author: windows-sdk-content
description: The ITuningSpaces interface represents a collection of tuning spaces.
old-location: mstv\ituningspaces.htm
tech.root: mstv
ms.assetid: db252e22-8efe-4bfc-8fd3-2be7022bbbbd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITuningSpaces, ITuningSpaces interface [Microsoft TV Technologies], ITuningSpaces interface [Microsoft TV Technologies],described, ITuningSpacesInterface, mstv.ituningspaces, tuner/ITuningSpaces
ms.topic: interface
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
 - ITuningSpaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuningSpaces interface


## -description



The <b>ITuningSpaces</b> interface represents a collection of tuning spaces.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuningSpaces</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITuningSpaces</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITuningSpaces</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspaces-get__newenum">get__NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection. (For use by Automation clients.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspaces-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Returns the number of tuning spaces in this collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspaces-get_enumtuningspaces">get_EnumTuningSpaces</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection. (For use by C++ clients.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspaces-get_item">get_Item</a>
</td>
<td align="left" width="63%">
Returns a specified item in the collection.

</td>
</tr>
</table> 


## -remarks



This interface is used to enumerate subsets of tuning spaces within the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/systemtuningspaces-object">SystemTuningSpaces</a> object. To enumerate all of the tuning spaces available on the system, use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer</a> interface on the SystemTuningSpaces object.

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuningSpaces)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

