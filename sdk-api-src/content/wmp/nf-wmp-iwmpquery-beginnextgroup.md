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

# IWMPQuery::beginNextGroup


## -description



The <b>beginNextGroup</b> method begins a new condition group.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Beginning a new condition group implies that you have completed the current condition group. The new condition group is always concatenated to the previous condition group by using OR logic.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/b1e6bf08-3b81-4c04-92ff-73eac5f7495a">IWMPMediaCollection2::createQuery</a>



<a href="https://msdn.microsoft.com/b3d4586b-c999-447c-b974-15bd0ef160a6">IWMPMediaCollection2::getPlaylistByQuery</a>



<a href="https://msdn.microsoft.com/070bc947-bf2b-4c06-9ffa-6a23625d178a">IWMPMediaCollection2::getStringCollectionByQuery</a>



<a href="https://msdn.microsoft.com/f1f3c46f-4756-49b4-ad4f-a9097ff787f8">IWMPQuery Interface</a>
 

 

