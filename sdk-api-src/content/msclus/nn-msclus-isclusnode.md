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

# ISClusNode interface


## -description


<p class="CCE_Message">[The <b>ClusNode</b> object is 
    available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in 
    subsequent versions.]

Enables operations on a 
    <a href="https://msdn.microsoft.com/4381e378-7bf2-4dbc-b56e-3fed33193d32">node</a>, its properties, and related objects.
<table>
<tr>
<th>Method or property</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a> Property</td>
<td>Returns a <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">Cluster</a> object providing access to the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/dn922625">cluster</a> associated with the node.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/976be45f-39dd-46ee-b558-026afa129b21">CommonProperties</a> Property</td>
<td>Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
      containing the node's read/write <a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common properties</a>.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c7bb2e51-81da-4848-9c0b-42ab711a5c62">CommonROProperties</a> Property</td>
<td>Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
      containing the node's read-only 
      <a href="https://msdn.microsoft.com/5341d390-69dd-4e84-a443-f35a4b6c0bab">common properties</a>.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e65a230e-3931-4e1a-b80d-3fd2499d330c">Evict</a> Method</td>
<td>Removes a node from the cluster.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/98799b21-6646-430c-8194-debc7985fa9d">NetInterfaces</a> Property</td>
<td>Returns a 
      <a href="https://msdn.microsoft.com/d40bd8bd-b822-4069-bc9c-b7fefc66c8d0">ClusNodeNetInterfaces</a> collection 
      providing access to the <a href="https://msdn.microsoft.com/cc0cbbc3-e342-483e-9c94-4ee43f4d588d">network interfaces</a> available 
      to the node.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8ef68a5e-e7a0-4b32-8649-4fd194520ea6">NodeID</a> Property</td>
<td>Returns the identifier of the node.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451189">Pause</a> Method</td>
<td>Temporarily suspends the cluster activity of the node.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/33520afe-ec3e-41dc-ad16-aaee4f5394aa">PrivateProperties</a> Property</td>
<td>Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
      containing the node's read/write 
      <a href="https://msdn.microsoft.com/a1dee11c-f1fe-4509-a40a-a58c4b8999ef">private properties</a>.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/146471dd-49f9-442c-a888-148fd86c4050">PrivateROProperties</a> Property</td>
<td>Returns a <a href="https://msdn.microsoft.com/b117b0eb-e188-4514-8e11-9acca1303e8f">ClusProperties</a> collection 
      containing the node's read-only private properties.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/45eae46b-54d2-4945-aab1-8b471df64881">ResourceGroups</a> Property</td>
<td>Returns a <a href="https://msdn.microsoft.com/7411d5f9-15c0-4c03-9128-c6b636979a50">ClusResGroups</a> collection 
      providing access to the <a href="https://msdn.microsoft.com/1e0680ba-87d0-4bf0-808c-d80485e4daa3">groups</a> that are currently being hosted by 
      the node.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/74e465e2-1328-4e05-b287-3ce27359c67a">Resume</a> Method</td>
<td>Resumes the cluster activity of the node.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c1887055-518a-4177-a618-418c75883d69">State</a> Property</td>
<td>Returns the state of the node.</td>
</tr>
</table> 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ClusNode</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ClusNode</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74e465e2-1328-4e05-b287-3ce27359c67a">Resume</a>
</td>
<td align="left" width="63%">
Resumes the cluster activity of the node.

</td>
</tr>
</table> 


## -remarks



A <b>ClusNode</b> object is obtained from the following 
    collections.

<ul>
<li>
<a href="https://msdn.microsoft.com/f35d610f-014a-48cf-aaa4-93e320bcd890">ClusNodes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3425825e-890c-4d3d-919e-a66963e1fc55">ClusResGroupPreferredOwnerNodes</a>
</li>
<li>
<a href="https://msdn.microsoft.com/a3269288-f32f-45d5-8fd4-4e6fb257c1be">ClusResPossibleOwnerNodes</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/8bf2124b-7e29-493c-a1ac-12e5f1cf5fe6">Node Management Objects</a>
 

 

