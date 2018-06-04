---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITextStoreACPServices interface


## -description


The <b>ITextStoreACPServices</b> interface is implemented by the TSF manager to provide various services to an ACP-based application. To obtain an instance of this interface, an application calls <b>QueryInterface</b> on the <i>punk</i> parameter passed to <a href="https://msdn.microsoft.com/aadf54e4-25ba-4280-a184-e1d2a2594c3c">ITextStoreACP::AdviseSink</a> with IID_ITextStoreACPServices.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextStoreACPServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITextStoreACPServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextStoreACPServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/727945e7-b876-460e-9b06-8d03734f53b2">CreateRange</a>
</td>
<td align="left" width="63%">
Creates a range object from two ACP values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6792ccc0-7bbd-479c-9f24-a283ce03c7fe">ForceLoadProperty</a>
</td>
<td align="left" width="63%">
Forces all values of an asynchronously loaded property to be loaded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14be52d1-4f8c-4deb-aa92-470c3608c841">Serialize</a>
</td>
<td align="left" width="63%">
Obtains a property from a range of text and writes the property data into a stream object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4eb2f2b9-51fb-4970-a195-c05e1d19ff99">Unserialize</a>
</td>
<td align="left" width="63%">
Takes previously serialized property data and applies it to a property object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/aadf54e4-25ba-4280-a184-e1d2a2594c3c">ITextStoreACP::AdviseSink
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

