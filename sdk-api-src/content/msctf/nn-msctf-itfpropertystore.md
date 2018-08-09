---
UID: NN:msctf.ITfPropertyStore
title: ITfPropertyStore
author: windows-sdk-content
description: The ITfPropertyStore interface is implemented by a text service and used by the TSF manager to provide non-static property values. An instance of this interface is passed to ITfProperty::SetValueStore.
old-location: tsf\itfpropertystore.htm
old-project: TSF
ms.assetid: 0678e622-3733-499b-b289-c8c181d4638c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfPropertyStore, ITfPropertyStore interface [Text Services Framework], ITfPropertyStore interface [Text Services Framework],described, _tsf_itfpropertystore_ref, msctf/ITfPropertyStore, tsf.itfpropertystore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfPropertyStore
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfPropertyStore interface


## -description


The <b>ITfPropertyStore</b> interface is implemented by a text service and used by the TSF manager to provide non-static property values. An instance of this interface is passed to <a href="https://msdn.microsoft.com/146af429-54a8-41b6-b44e-b5d35f933435">ITfProperty::SetValueStore</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfPropertyStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfPropertyStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfPropertyStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates an exact copy of the property store object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b982cb1-e1b6-440b-9ac6-9b34bb86731d">Divide</a>
</td>
<td align="left" width="63%">
Called when the text covered by the property is split into two ranges.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn949631">GetData</a>
</td>
<td align="left" width="63%">
Obtains the property store data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/700c704f-d336-443d-825b-cb376bba966c">GetDataType</a>
</td>
<td align="left" width="63%">
This method is reserved, but must be implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94fa2e8f-5bdd-4ec0-b632-269d4a7b3f73">GetPropertyRangeCreator</a>
</td>
<td align="left" width="63%">
Obtains the class identifier of the property store owner.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Obtains the property identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e3d6341-6e5b-445e-b6ac-48853a5b56f2">OnTextUpdated</a>
</td>
<td align="left" width="63%">
Called when the text that the property store applies to is modified.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b84bce22-684f-4326-9e28-0fc16b818732">Serialize</a>
</td>
<td align="left" width="63%">
Called to write the property store data into a stream for serialization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55637d69-2f1a-435d-be23-4c29ec57b2ea">Shrink</a>
</td>
<td align="left" width="63%">
Called when the text that the property store applies to is truncated.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/146af429-54a8-41b6-b44e-b5d35f933435">ITfProperty::SetValueStore
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

