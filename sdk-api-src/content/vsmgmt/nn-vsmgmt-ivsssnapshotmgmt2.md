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

# IVssSnapshotMgmt2 interface


## -description


The <b>IVssSnapshotMgmt2</b> interface 
    provides a method to retrieve the minimum size of the shadow copy storage area.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssSnapshotMgmt2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssSnapshotMgmt2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssSnapshotMgmt2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1ee4499-07cb-4373-a3c9-892129a257db">GetMinDiffAreaSize</a>
</td>
<td align="left" width="63%">
Returns the current minimum size of the shadow copy storage area.</p> (Inherited from <b>IVssSnapshotMgmt2</b>)</td>
</tr>
</table> 


## -remarks



To obtain an instance of the <b>IVssSnapshotMgmt2</b> 
   interface, call the <a href="_com_iunknown_queryinterface">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/5e5694a1-7c17-4d8a-b094-09dcf28a636f">IVssSnapshotMgmt</a> interface, passing 
   <b>IID_IVssSnapshotMgmt2</b> as the <i>riid</i> parameter.




## -see-also




<a href="_com_iunknown">IUnknown</a>



<a href="https://msdn.microsoft.com/3a0c60df-666c-4e33-a54c-7fa5ddbfde13">Volume Shadow Copy API Interfaces</a>
 

 

