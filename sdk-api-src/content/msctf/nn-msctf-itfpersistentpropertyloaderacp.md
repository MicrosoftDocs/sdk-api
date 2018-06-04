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

# ITfPersistentPropertyLoaderACP interface


## -description


The <b>ITfPersistentPropertyLoaderACP</b> interface is implemented by an application and used by the TSF manager to load properties asynchronously. An application passes an instance of this interface when calling <a href="https://msdn.microsoft.com/4eb2f2b9-51fb-4970-a195-c05e1d19ff99">ITextStoreACPServices::Unserialize</a>. When properties are loaded by a call to <b>ITextStoreACPServices::Unserialize</b> , this interface is used to load properties when required rather than all at once.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfPersistentPropertyLoaderACP</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfPersistentPropertyLoaderACP</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfPersistentPropertyLoaderACP</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/20730a90-e59c-46ae-a0bf-a212b201351c">LoadProperty</a>
</td>
<td align="left" width="63%">
Called to load a property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4eb2f2b9-51fb-4970-a195-c05e1d19ff99">ITextStoreACPServices::Unserialize
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

