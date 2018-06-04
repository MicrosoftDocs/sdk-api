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

# IAttachmentExecute::CheckPolicy


## -description


Provides a Boolean test that can be used to make decisions based on the attachment's execution policy.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns one of the following values.
                    

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>Enable</td>
</tr>
<tr>
<td>S_FALSE</td>
<td>Prompt</td>
</tr>
<tr>
<td>Any other failure code</td>
<td>Disable</td>
</tr>
</table>
 




## -remarks



<b>IAttachmentExecute::CheckPolicy</b> examines a set of properties known collectively as <i>evidence</i>. Anything used to determine trust level is considered evidence. These properties are set using the following methods.

				

<ul>
<li>
<a href="https://msdn.microsoft.com/52dc823f-4429-4c1f-8906-9e4ee3f8158e">IAttachmentExecute::SetFileName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/763ce5a7-bbad-4dd8-a416-86a96f466510">IAttachmentExecute::SetLocalPath</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d7ee869a-2afe-4d98-a0bb-d80e57425079">IAttachmentExecute::SetReferrer</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6545252b-1c43-4d62-9784-b63688ef9fdc">IAttachmentExecute::SetSource</a>
</li>
</ul>


				The information returned by <b>IAttachmentExecute::CheckPolicy</b> enables an application to modify its UI appropriately for the situation.
			

<b>IAttachmentExecute::CheckPolicy</b> requires the application first to call either <a href="https://msdn.microsoft.com/52dc823f-4429-4c1f-8906-9e4ee3f8158e">IAttachmentExecute::SetFileName</a> or <a href="https://msdn.microsoft.com/763ce5a7-bbad-4dd8-a416-86a96f466510">IAttachmentExecute::SetLocalPath</a>.



