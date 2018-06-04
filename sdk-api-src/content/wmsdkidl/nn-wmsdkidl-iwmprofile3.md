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

# IWMProfile3 interface


## -description



The <b>IWMProfile3</b> interface provides enhanced features for profiles. This includes the ability to create two new types of objects: bandwidth sharing objects and stream prioritization objects.

An <b>IWMProfile3</b> interface is created for each profile object created. You can retrieve a pointer to an <b>IWMProfile3</b> interface by calling the <b>QueryInterface</b> method of any other interface of the profile. You can also access <b>IWMProfile3</b> from a reader or synchronous reader object by calling the <b>QueryInterface</b> method of an existing interface in the object. For more information, see <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfile3</b> interface inherits from <a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>. <b>IWMProfile3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMProfile3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/174a4583-93fb-41cd-ba14-a959a28c1ea3">AddBandwidthSharing</a>
</td>
<td align="left" width="63%">
Adds an existing bandwidth sharing object to the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab6c9903-95ea-499b-be75-ff57328336f0">CreateNewBandwidthSharing</a>
</td>
<td align="left" width="63%">
Creates a new bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/801a66fa-b72d-4282-953e-216fb9a56cd7">CreateNewStreamPrioritization</a>
</td>
<td align="left" width="63%">
Creates a new stream prioritization object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be66ff8b-c883-4329-aaa4-e9549d0cbb9e">GetBandwidthSharing</a>
</td>
<td align="left" width="63%">
Obtains a pointer to the <b>IWMBandwidthSharing</b> interface of an existing bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f5a11a7-d81a-4ca1-8b0f-1d561f736523">GetBandwidthSharingCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of bandwidth sharing objects that exist in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ddab3735-06a1-4e03-9abc-0fca635ef759">GetExpectedPacketCount</a>
</td>
<td align="left" width="63%">
Retrieves the expected number of <a href="wmformat_glossary.htm">packets</a> for a specified duration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42aea1df-63cd-4eda-86c8-3cebe92d5c82">GetStorageFormat</a>
</td>
<td align="left" width="63%">

          Not implemented in this release.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09545c1e-8090-4526-9faf-6cb2cb369208">GetStreamPrioritization</a>
</td>
<td align="left" width="63%">
Retrieves the stream prioritization object associated with the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c0a90aa-154a-49c9-ab8e-0d1c4ce02641">RemoveBandwidthSharing</a>
</td>
<td align="left" width="63%">
Removes a bandwidth sharing object from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1522cb9f-ce3f-4183-8779-3ee112efb40b">RemoveStreamPrioritization</a>
</td>
<td align="left" width="63%">
Removes a stream prioritization object from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43cbb36f-ec00-48e5-9182-b69e8c196ab0">SetStorageFormat</a>
</td>
<td align="left" width="63%">

          Not implemented in this release.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16dfb205-2a0b-4dc8-a8f2-8981534018f1">SetStreamPrioritization</a>
</td>
<td align="left" width="63%">
Assigns a stream prioritization object to the profile.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://msdn.microsoft.com/9dc863da-1842-41e7-b66c-c97e0140046d">Bandwidth Sharing Object</a>



<a href="https://msdn.microsoft.com/fd0e48bb-2e5e-4158-9ff1-5b603f219689">IWMBandwidthSharing Interface</a>



<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2 Interface</a>



<a href="https://msdn.microsoft.com/ef8ae275-c36a-492c-b57c-d640044ede93">IWMStreamPrioritization Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/cb0345ce-6847-435b-8cbb-f8b93856af9f">Stream Prioritization Object</a>
 

 

