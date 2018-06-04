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

# IWICProgressiveLevelControl interface


## -description


Exposes methods for obtaining information about and controlling progressive decoding.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWICProgressiveLevelControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWICProgressiveLevelControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWICProgressiveLevelControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6f848a0-e373-4344-8923-3ad77165ef71">GetCurrentLevel</a>
</td>
<td align="left" width="63%">
Gets the last level set by the <a href="https://msdn.microsoft.com/b4a2c279-385d-4177-bd8f-a49f545c692a">SetCurrentLevel</a> call.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7949d31-c679-43ea-aa07-5f9f8579b4f7">GetLevelCount</a>
</td>
<td align="left" width="63%">
Gets the number of levels of progressive decoding supported by the CODEC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4a2c279-385d-4177-bd8f-a49f545c692a">SetCurrentLevel</a>
</td>
<td align="left" width="63%">
Specifies the level to retrieve on the next call to <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">CopyPixels</a>.

</td>
</tr>
</table> 


## -remarks



Images can only be progressively decoded if they were progressively encoded. Progressive images automatically start at the highest (best quality) progressive level. The caller must manually set the decoder to a lower progressive level.

E_NOTIMPL is returned if the codec does not support progressive level decoding.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d22c2c59-0fa1-4452-93f1-dbf151033714">Progressive Decoding Overview</a>



<a href="https://msdn.microsoft.com/14018dce-26f0-4e1e-9d19-c5b42dd2cdab">WIC Progressive Decoding Sample</a>
 

 

