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

# ITfContextView interface


## -description


The <b>ITfContextView</b> interface is implemented by the TSF manager and used by a client (application or text service) to obtain information about a context view. Clients obtain this interface by calling the <a href="https://msdn.microsoft.com/41f7eb74-bca2-4d53-8a70-0b872616fd1b">ITfContext::GetActiveView</a> method which returns a pointer to the <b>ITfContextView</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfContextView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfContextView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfContextView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/543761fe-420e-4821-a69f-abc6c853677e">GetRangeFromPoint</a>
</td>
<td align="left" width="63%">
Converts a point, in screen coordinates, to an empty range positioned at a corresponding location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/86dde611-4c46-418c-aa89-728081a28943">GetScreenExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box of the display surface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4ef9180-5568-4e5b-8c37-f750263060d2">GetTextExt</a>
</td>
<td align="left" width="63%">
Returns the bounding box, in screen coordinates, of a range of text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e805842d-4737-45be-8314-bd83d94da2d6">GetWnd</a>
</td>
<td align="left" width="63%">
Returns an HWND that corresponds to the document, if one exists.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
        
      </a>



<a href="_COM_IUnknown">IUnknown</a>
 

 

