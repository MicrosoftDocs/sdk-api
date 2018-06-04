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

# IMenuBand::TranslateMenuMessage


## -description


Translates a message for a Component Object Model (COM) object.


## -parameters




### -param pmsg [in, out]

Type: <b><a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/fee176ba-ad07-4145-ab4d-1b8c335fd100">MSG</a> structure that contains the incoming message.


### -param plRet [out]

Type: <b>LRESULT*</b>

A pointer to the translated message.


## -returns



Type: <b>HRESULT</b>

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The message was handled and should be deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The message was not handled. In this case, *plRet is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



Typically, <a href="https://msdn.microsoft.com/d30a456c-7c09-4250-8509-353c54d017b9">IMenuBand::IsMenuMessage</a> is called before this method. The parent window proc, not the message pump, must call <b>IMenuBand::TranslateMenuMessage</b> for every message.

This method can change the values of <i>pmsg</i>. If so, the changes should be forwarded on.

This method is required because some modal message pumps do not allow a call to a custom translation method.



