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

# IWMIndexer2 interface


## -description



The <b>IWMIndexer2</b> interface enables you to change the settings of the indexer object to suit your needs.

This interface is implemented as part of the indexer object. To obtain a pointer to <b>IWMIndexer2</b>, call the <b>QueryInterface</b> method of the <b>IWMIndexer</b> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMIndexer2</b> interface inherits from <a href="https://msdn.microsoft.com/00627b0c-4484-417a-8680-0fd97aac41fe">IWMIndexer</a>. <b>IWMIndexer2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMIndexer2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4ab9ad8-5fc7-43ce-ba2f-f32135a44a86">Configure</a>
</td>
<td align="left" width="63%">
Enables custom configuration of the indexer object.

</td>
</tr>
</table> 

The following interface can be obtained by using the QueryInterface method of this interface.

<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/00627b0c-4484-417a-8680-0fd97aac41fe">IWMIndexer</a>
</td>
<td>IID_IWMIndexer</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/00627b0c-4484-417a-8680-0fd97aac41fe">IWMIndexer Interface</a>



<a href="https://msdn.microsoft.com/652e04a5-ed6e-4e92-acf4-55ed82f77ef1">Indexer Object</a>
 

 

