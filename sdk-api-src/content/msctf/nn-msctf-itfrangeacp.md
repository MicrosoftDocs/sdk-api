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

# ITfRangeACP interface


## -description


The <b>ITfRangeACP</b> interface is implemented by the TSF manager and is used by an application character position (ACP)-based application to access and manipulate range objects. This interface is derived from the <a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange</a> interface. Obtain an instance of this interface by querying an <b>ITfRange</b> object for IID_ITfRangeACP.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfRangeACP</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfRangeACP</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfRangeACP</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14838cea-1a19-4faa-ac7f-617fde82432d">GetExtent</a>
</td>
<td align="left" width="63%">
Obtains the application character position and length of the range object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b409ba8-dce6-4b42-8cfe-f159de1cad2c">SetExtent</a>
</td>
<td align="left" width="63%">
Sets the application character position and length of the range object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b8889f7d-3228-4ecc-8d24-c04234d3101e">ITfRange
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

