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

# ITfIntegratableCandidateListUIElement::SetIntegrationStyle


## -description


Sets the integration style.


## -parameters




### -param guidIntegrationStyle [in]

The desired type of keyboard integration experience.


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
The text service supports the integration style.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The text service does not support the integration style.

</td>
</tr>
</table>
 




## -remarks



If an app needs a keyboard-integrated experience, it can set a <b>GUID</b> for the desired type of 
    integration experience.  If the text service supports the integration style, it should return <b>S_OK</b>.
          If it's not supported, it should return <b>E_NOTIMPL</b>.  When called, the text service may adjust its respond to
    keyboard interaction for the lifetime of the <a href="https://msdn.microsoft.com/1f39aa06-3c94-4959-b857-ca61498d5b5c">ITfCandidateListUIElement</a> object, for example, until <a href="https://msdn.microsoft.com/b29539fe-a240-498b-8267-be243d437005">ITfUIElementSink::EndUIElement</a> is called.




## -see-also




<a href="https://msdn.microsoft.com/F9AB2037-6806-42FC-BD41-F6B6BA047908">ITfIntegratableCandidateListUIElement</a>



<a href="https://msdn.microsoft.com/b29539fe-a240-498b-8267-be243d437005">ITfUIElementSink::EndUIElement</a>
 

 

