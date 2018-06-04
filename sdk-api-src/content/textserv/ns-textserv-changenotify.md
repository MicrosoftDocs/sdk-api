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

# CHANGENOTIFY structure


## -description


Contains information that is associated with an <a href="https://msdn.microsoft.com/97C0D9F1-7D4E-409D-A4F6-E645475A8EEF">EN_CHANGE</a> notification code. A windowless rich edit control sends this notification to its host window when the content of the control changes.


## -struct-fields




### -field dwChangeType

The type of change that occurred. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CN_GENERIC"></a><a id="cn_generic"></a><dl>
<dt><b>CN_GENERIC</b></dt>
</dl>
</td>
<td width="60%">
No significant change occurred.

</td>
</tr>
<tr>
<td width="40%"><a id="CN_NEWREDO"></a><a id="cn_newredo"></a><dl>
<dt><b>CN_NEWREDO</b></dt>
</dl>
</td>
<td width="60%">
A new redo action was added.

</td>
</tr>
<tr>
<td width="40%"><a id="CN_NEWUNDO"></a><a id="cn_newundo"></a><dl>
<dt><b>CN_NEWUNDO</b></dt>
</dl>
</td>
<td width="60%">
A new undo action was added.

</td>
</tr>
<tr>
<td width="40%"><a id="CN_TEXTCHANGED"></a><a id="cn_textchanged"></a><dl>
<dt><b>CN_TEXTCHANGED</b></dt>
</dl>
</td>
<td width="60%">
The text changed.

</td>
</tr>
</table>
 


### -field pvCookieData

Cookie for the undo action 
										that is associated with the change.


## -see-also




<a href="https://msdn.microsoft.com/97C0D9F1-7D4E-409D-A4F6-E645475A8EEF">EN_CHANGE</a>
 

 

