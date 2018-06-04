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

# ITfContextOwner::GetScreenExt


## -description


The <b>ITfContextOwner::GetScreenExt</b> method returns the bounding box, in screen coordinates, of the display surface where the text stream is rendered.


## -parameters




### -param prc [out]

Receives the bounding box screen coordinates of the display surface of the document.


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



If the text is not currently displayed, for example if the document window is minimized, <i>prc</i> is set to { 0, 0, 0, 0 }.




## -see-also




<a href="https://msdn.microsoft.com/bd542dd1-79a5-47ec-a563-cd37a8c36b1a">
        ITextStoreACP::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/630646df-dd47-4dbf-9787-f9d697ad8d7a">ITfContextOwner</a>



<a href="https://msdn.microsoft.com/86dde611-4c46-418c-aa89-728081a28943">ITfContextView::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">
        TsViewCookie
      </a>
 

 

