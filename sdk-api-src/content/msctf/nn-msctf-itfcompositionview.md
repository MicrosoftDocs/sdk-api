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

# ITfCompositionView interface


## -description


The <b>ITfCompositionView</b> interface is implemented by the TSF manager and used by an application to obtain data about a composition view. An instance of this interface is provided by one of the <a href="https://msdn.microsoft.com/4fea0a48-df5f-4f34-a3ea-d52883f6f8b1">ITfContextOwnerCompositionSink</a> methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfCompositionView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfCompositionView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfCompositionView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1435e083-c6a1-491c-a7c2-7d2cb1d54508">GetOwnerClsid</a>
</td>
<td align="left" width="63%">
Obtains the class identifier of the text service that created the composition object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31372688-be81-4883-9fc7-ed3f7b2f7934">GetRange</a>
</td>
<td align="left" width="63%">
Obtains a range object that contains the text covered by the composition.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4fea0a48-df5f-4f34-a3ea-d52883f6f8b1">ITfContextOwnerCompositionSink
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

