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

# ISyncKnowledge2 interface


## -description


Represents additional information about the knowledge that a replica has about its item store.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncKnowledge2</b> interface inherits from <a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge</a>. <b>ISyncKnowledge2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncKnowledge2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1649f70-8c8b-4eea-8ecb-7ea5a657eabe">CompareToKnowledgeCookie</a>
</td>
<td align="left" width="63%">
Performs a fast comparison between the specified knowledge cookie and this knowledge object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12ad8a10-1edb-4ba0-9a16-64fe9fda0125">Complement</a>
</td>
<td align="left" width="63%">
Returns the knowledge that is contained in this object but that is not contained in the specified knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecaefb24-eca0-408c-a98d-f7e6bbfefade">ContainsKnowledgeForChangeUnit</a>
</td>
<td align="left" width="63%">
Indicates whether the specified knowledge of the specified change unit is known by this knowledge.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5359e50d-8541-40ed-8107-a904ac62bfe0">ContainsKnowledgeForItem</a>
</td>
<td align="left" width="63%">
Indicates whether the specified knowledge of the specified item is known by this knowledge.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbb049b8-cd2c-49f3-a9f9-0d76da0b3824">GetIdParameters</a>
</td>
<td align="left" width="63%">
Gets the ID format schema of the provider.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/088d864f-bb74-4fd8-b8cb-352cb2731edb">GetInspector</a>
</td>
<td align="left" width="63%">
Returns an object that can be used to retrieve the contents of the knowledge object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d182f81d-131c-4f18-85e4-ff675ae99888">GetKnowledgeCookie</a>
</td>
<td align="left" width="63%">
Gets a lightweight, read-only representation of this knowledge object that can be used for fast comparisons.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06a1a380-3fe8-4c99-be97-d84b6be9838d">GetLowestUncontainedId</a>
</td>
<td align="left" width="63%">
Returns the lowest item ID that is contained in the specified knowledge and that is not contained in this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06b5794e-ba46-499f-b85c-f0acb4fd79a7">GetMinimumSupportedVersion</a>
</td>
<td align="left" width="63%">
Gets the minimum supported version of Microsoft Sync Framework components that can be used with this object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7dea268-87d7-4e6d-9618-089036d52699">GetStatistics</a>
</td>
<td align="left" width="63%">
Gets the specified statistic data that is contained in this object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d2ce743-7827-4ee4-a800-3ba706d4a7a6">IntersectsWithKnowledge</a>
</td>
<td align="left" width="63%">
Indicates whether the specified knowledge intersects with this knowledge.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe183377-9b5a-476b-91af-ff974a9d41a4">ProjectOntoColumnSet</a>
</td>
<td align="left" width="63%">
Returns the knowledge for the specified set of change units for all the items that are contained in this object.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71794c37-fea2-466b-a8dd-8a502b178f1b">ProjectOntoKnowledgeWithPrerequisite</a>
</td>
<td align="left" width="63%">
Returns knowledge about the knowledge fragments that are specified by the template knowledge, when the template knowledge contains the prerequisite knowledge for the specified fragments. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8b9084f-f4aa-42b8-8c45-ed075db8ffe4">SerializeWithOptions</a>
</td>
<td align="left" width="63%">
Serializes the knowledge object data to a byte array based on the specified version and serialization options.


</td>
</tr>
</table> 


## -remarks



An <b>ISyncKnowledge2</b> object can be obtained by passing <b>IID_ISyncKnowledge2</b> to the <b>QueryInterface</b> method of an <b>ISyncKnowledge</b> object.




## -see-also




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

