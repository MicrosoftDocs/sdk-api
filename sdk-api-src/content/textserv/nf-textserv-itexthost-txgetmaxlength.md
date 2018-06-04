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

# ITextHost::TxGetMaxLength


## -description


Gets the text host's maximum allowed length for the text.


## -parameters




### -param plength






#### - pLength

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The maximum allowed text length, in number of characters. If INFINITE is returned, the text services object can use as much memory as needed to store any specified text. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

The return value is <b>S_OK</b>.




## -remarks



When this maximum is reached, the text services object should reject any further character insertion and pasted text. 
				<a href="https://msdn.microsoft.com/29be3eba-285c-4297-b692-0a5fcb4797c6">TxSetText</a> however should still accept (and set) text longer than the maximum length. This is because this method is used for binding and is critical to maintaining the integrity of the data to which the control is bound.

This method parallels the <a href="https://msdn.microsoft.com/5a605de7-8dc7-4c54-8f18-e0b08c720856">EM_LIMITTEXT</a> message. 

If the limit returned is less than the number of characters currently in the text services object, no data is lost. Instead, no edits are allowed to the text 
				<i>other</i> than deletion until the text is reduced to below the limit.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/5a605de7-8dc7-4c54-8f18-e0b08c720856">EM_LIMITTEXT</a>



<a href="https://msdn.microsoft.com/28d86b94-2d36-4749-8954-3857bf6dbdac">ITextHost</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/71ecd220-ab1a-4caa-b1b9-0951e943692e">Windowless Rich Edit Controls</a>
 

 

