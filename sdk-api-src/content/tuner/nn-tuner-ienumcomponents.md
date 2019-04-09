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
---

# IEnumComponents interface


## -description



The <b>IEnumComponents</b> interface provides a standard COM enumeration object for the components (substreams) in a given program stream. C++ applications should use this interface to enumerate components, rather than using the <a href="https://msdn.microsoft.com/670b47ba-bcbd-4281-95e3-a5d784f0610b">IComponents</a> collection interface, which is intended for Automation clients.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumComponents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumComponents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ca15a67e-1788-4f57-bfe8-ec1a3014044f">Clone</a>
</td>
<td align="left" width="63%">
Create a new copy of the entire collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73cb45c7-1f74-46cf-a410-ec1d5fed4271">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next <i>n</i> elements in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/753c9f74-3a97-4a8f-ba76-21e7b1d77a70">Reset</a>
</td>
<td align="left" width="63%">
Reset the enumerator to the beginning of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f63eca00-c47c-4b9f-8f7a-7080c23653ce">Skip</a>
</td>
<td align="left" width="63%">
Skip the specified element in the collection without retrieving it.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumComponents)</code>.




## -see-also




<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

