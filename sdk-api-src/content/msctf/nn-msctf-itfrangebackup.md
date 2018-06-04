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

# ITfRangeBackup interface


## -description


The <b>ITfRangeBackup</b> interface is implemented by the TSF manager and is used by a text service to create a backup copy of the data contained in a range object. This backup copy can be used later to restore the range object. An instance of this interface is obtained by calling <a href="https://msdn.microsoft.com/c3b52170-af1b-407b-9160-1265ae3c9afc">ITfContext::CreateRangeBackup</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfRangeBackup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfRangeBackup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfRangeBackup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb168504-34c0-4d30-826e-61926fd10a2a">Restore</a>
</td>
<td align="left" width="63%">
Restores a specified range object into the TSF context.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c3b52170-af1b-407b-9160-1265ae3c9afc">ITfContext::CreateRangeBackup
      </a>



<a href="https://msdn.microsoft.com/2b85012f-b090-4c91-b29c-b2470ff63ab6">ITfRange::Clone
      </a>



<a href="_COM_IUnknown">IUnknown</a>



<a href="ranges.htm">Ranges: Clones and Backups</a>
 

 

