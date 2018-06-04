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

# IWMDMStorageControl3 interface


## -description



The <b>IWMDMStorageControl3</b> interface extends <b>IWMDMStorageControl2</b> by providing an <b>Insert</b> method that accepts an <a href="https://msdn.microsoft.com/ea57a851-0b9f-444c-9819-a278f2ece2b0">IWMDMMetaData</a> interface pointer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorageControl3</b> interface inherits from <a href="https://msdn.microsoft.com/c5a17642-5253-4d01-895a-09d00284f341">IWMDMStorageControl2</a>. <b>IWMDMStorageControl3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorageControl3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/044a6571-8ec0-48af-b105-07c60c25d68a">Insert3</a>
</td>
<td align="left" width="63%">
Puts content into/next to the storage. Extends <a href="https://msdn.microsoft.com/bc6cc03c-e13a-45d8-afcb-1fadd5f4dd8e">IWMDMStorageControl2::Insert2</a> method by allowing the application to pass in an <b>IWMDMMetaData</b> interface pointer.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl Interface</a>



<a href="https://msdn.microsoft.com/c5a17642-5253-4d01-895a-09d00284f341">IWMDMStorageControl2 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

