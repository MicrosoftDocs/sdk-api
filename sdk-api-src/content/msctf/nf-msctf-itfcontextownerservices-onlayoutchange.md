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

# ITfContextOwnerServices::OnLayoutChange


## -description


The <b>ITfContextOwnerServices::OnLayoutChange</b> method is called by the context owner when the on-screen representation of the text stream is updated during a composition. Text stream updates include when the position of the window that contains the text is changed or if the screen coordinates of the text change.


## -parameters






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



A call to <b>ITfContextOwnerServices::OnLayoutChange</b> could be in response to a text edit, font size change, window movement/resizing, and so on.

If a call to <a href="https://msdn.microsoft.com/d621e96b-d357-4468-8a89-89445fb1ca9e">ITfContextView::GetTextExt</a> or <a href="https://msdn.microsoft.com/b6489391-a19e-405a-a129-f68054088860">ITfContextOwner::GetACPFromPoint</a> fails because the application did not calculate the screen layout (Return Value: TS_E_NOLAYOUT), the application must then call <b>ITfContextOwnerServices::OnLayoutChange</b> when the information is ready.




## -see-also




<a href="https://msdn.microsoft.com/b6489391-a19e-405a-a129-f68054088860">ITfContextOwner::GetACPFromPoint
      </a>



<a href="https://msdn.microsoft.com/fb77bd6a-ae34-4e21-8f09-fc8c6a1ade86">ITfContextOwnerServices</a>



<a href="https://msdn.microsoft.com/d621e96b-d357-4468-8a89-89445fb1ca9e">
        ITfContextView::GetTextExt
      </a>
 

 

