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

# _endcomposition structure


## -description


Contains information about an EN_ENDCOMPOSITION notification code from a rich edit control. 




## -struct-fields




### -field nmhdr

The <b>code</b> member of this structure identifies the notification code being sent. 


### -field dwCode

Indicates the state of the composition. This member is one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ECN_ENDCOMPOSITION"></a><a id="ecn_endcomposition"></a><dl>
<dt><b>ECN_ENDCOMPOSITION</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The composition is complete.

</td>
</tr>
<tr>
<td width="40%"><a id="ECN_NEWTEXT"></a><a id="ecn_newtext"></a><dl>
<dt><b>ECN_NEWTEXT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
There are new characters in the composition.

</td>
</tr>
</table>
 

