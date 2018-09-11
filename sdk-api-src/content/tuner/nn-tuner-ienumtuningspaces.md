---
UID: NN:tuner.IEnumTuningSpaces
title: IEnumTuningSpaces
author: windows-sdk-content
description: The IEnumTuningSpaces interface is implemented on a standard COM collection of tuning space objects and is obtained through various ITuningSpaceContainer.
old-location: mstv\ienumtuningspaces.htm
tech.root: mstv
ms.assetid: 9b64a48f-ebab-46af-a89d-b8bc488d85da
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IEnumTuningSpaces, IEnumTuningSpaces interface [Microsoft TV Technologies], IEnumTuningSpaces interface [Microsoft TV Technologies],described, IEnumTuningSpacesInterface, mstv.ienumtuningspaces, tuner/IEnumTuningSpaces
ms.prod: windows
ms.technology: windows-sdk
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
 - IEnumTuningSpaces
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumTuningSpaces interface


## -description



The <b>IEnumTuningSpaces</b> interface is implemented on a standard COM collection of tuning space objects and is obtained through various <a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTuningSpaces</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTuningSpaces</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3f9ad46e-38a7-4f07-b04b-999c912f9965">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the collection and all its sub-objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1220d006-10e9-4e64-8a18-8828b62d5da9">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>n</i> element in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9ac5d70-11f8-4bb4-a873-94eb72ea2f42">Reset</a>
</td>
<td align="left" width="63%">
Moves the iterator to the beginning of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5449fca0-4b8d-402e-b444-e7bc314e47b3">Skip</a>
</td>
<td align="left" width="63%">
Skips the specified element in the collection.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumTuningSpaces)</code>.




## -see-also




<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

