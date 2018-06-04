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

# ITfContextView::GetScreenExt


## -description


The <b>ITfContextView::GetScreenExt</b> method returns the bounding box, in screen coordinates, of the document display.


## -parameters




### -param prc [out]

Receives the bounding box, in screen coordinates, of the display surface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>
 




## -remarks



The <i>prc</i> parameter is cleared to {0,0,0,0} if the document is not currently displayed.




## -see-also




<a href="https://msdn.microsoft.com/bd542dd1-79a5-47ec-a563-cd37a8c36b1a">
        ITextStoreACP::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/499a446d-1575-4636-b444-dd6078ed8736">ITfContextOwner::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/302d185d-dab7-4a77-a5cf-da2529d8b24a">ITfContextView</a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">
        TsViewCookie
      </a>
 

 

