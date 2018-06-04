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

# ITfLangBarItemMgr::UnadviseItemSink


## -description




## -parameters




### -param dwCookie [in]

Contains a <i>DWORD</i> that identifies the advise sink to remove. This cookie is obtained when the advise sink is installed with <a href="https://msdn.microsoft.com/c01d80eb-9156-4fbf-98ff-7f06b145e72f">ITfLangBarItemMgr::AdviseItemSink</a> or <a href="https://msdn.microsoft.com/c0a3e86b-487b-410a-8bba-c2b5126126d2">ITfLangBarItemMgr::AdviseItemsSink</a>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a7fa257f-e600-4554-8b23-f73323f37e69">ITfLangBarItemMgr</a>



<a href="https://msdn.microsoft.com/c01d80eb-9156-4fbf-98ff-7f06b145e72f">ITfLangBarItemMgr::AdviseItemSink
      </a>



<a href="https://msdn.microsoft.com/c0a3e86b-487b-410a-8bba-c2b5126126d2">
        ITfLangBarItemMgr::AdviseItemsSink
      </a>
 

 

