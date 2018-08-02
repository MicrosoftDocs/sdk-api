---
UID: NN:tuner.IComponents
title: IComponents
author: windows-sdk-content
description: The IComponents interface represents a collection of components.
old-location: mstv\icomponents.htm
old-project: mstv
ms.assetid: 670b47ba-bcbd-4281-95e3-a5d784f0610b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IComponents, IComponents interface [Microsoft TV Technologies], IComponents interface [Microsoft TV Technologies],described, IComponentsInterface, mstv.icomponents, tuner/IComponents
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
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IComponents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponents interface


## -description



The <b>IComponents</b> interface represents a collection of components. In digital television, the term <i>component</i> refers to a substream within the program stream. For example, a program stream may have three audio streams in different languages; in this case each audio stream is a component of the program stream. The <b>IComponents</b> interface is implemented on the Components object, which is a collection of components. The Components object enables applications to enumerate components within a program stream and perform operations related to individual components in the collection. The Components object also supports <b>IPersistPropertyBag</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComponents</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IComponents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComponents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds a Component object to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates a new copy of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/214030ff-8aec-46df-8b59-f31fe926d8aa">EnumComponents</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/8811021c-8c14-4be6-8802-76b942bb34d8">IEnumComponents</a> enumerator for all components in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcb965f4-8fd6-415f-8fb6-a80d0c92731d">get__NewEnum</a>
</td>
<td align="left" width="63%">
Enumeration method to support For…Each loops in Automation clients.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba198e27-c699-4c93-aa2d-b8be8c40380c">get_Count</a>
</td>
<td align="left" width="63%">
Gets the number of Component objects in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12716c7c-3156-401e-8f1c-be3100afb912">get_Item</a>
</td>
<td align="left" width="63%">
Enables the caller to access a component by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f38e844-d197-40c1-8715-ffe406274b3c">put_Item</a>
</td>
<td align="left" width="63%">
Replaces an existing item in the collection with a new Component object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes a Component object from the collection.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IComponents)</code>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

