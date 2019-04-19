---
UID: NN:wmsdkidl.IWMProfile3
title: IWMProfile3 (wmsdkidl.h)
author: windows-sdk-content
description: The IWMProfile3 interface provides enhanced features for profiles.
old-location: wmformat\iwmprofile3.htm
tech.root: wmformat
ms.assetid: 7942aa81-ada7-4e9c-a261-f257f8f890b7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMProfile3, IWMProfile3 interface [windows Media Format], IWMProfile3 interface [windows Media Format],described, IWMProfile3Interface, wmformat.iwmprofile3, wmsdkidl/IWMProfile3
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMProfile3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile3 interface


## -description



The <b>IWMProfile3</b> interface provides enhanced features for profiles. This includes the ability to create two new types of objects: bandwidth sharing objects and stream prioritization objects.

An <b>IWMProfile3</b> interface is created for each profile object created. You can retrieve a pointer to an <b>IWMProfile3</b> interface by calling the <b>QueryInterface</b> method of any other interface of the profile. You can also access <b>IWMProfile3</b> from a reader or synchronous reader object by calling the <b>QueryInterface</b> method of an existing interface in the object. For more information, see <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfile3</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Dd757266(v=VS.85).aspx">IWMProfile2</a>. <b>IWMProfile3</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Dd757269(v=VS.85).aspx">AddBandwidthSharing</a>
</td>
<td align="left" width="63%">
Adds an existing bandwidth sharing object to the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757270(v=VS.85).aspx">CreateNewBandwidthSharing</a>
</td>
<td align="left" width="63%">
Creates a new bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757271(v=VS.85).aspx">CreateNewStreamPrioritization</a>
</td>
<td align="left" width="63%">
Creates a new stream prioritization object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757272(v=VS.85).aspx">GetBandwidthSharing</a>
</td>
<td align="left" width="63%">
Obtains a pointer to the <b>IWMBandwidthSharing</b> interface of an existing bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757273(v=VS.85).aspx">GetBandwidthSharingCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of bandwidth sharing objects that exist in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757378(v=VS.85).aspx">GetExpectedPacketCount</a>
</td>
<td align="left" width="63%">
Retrieves the expected number of <a href="https://msdn.microsoft.com/en-us/library/Dd757828(v=VS.85).aspx">packets</a> for a specified duration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757379(v=VS.85).aspx">GetStorageFormat</a>
</td>
<td align="left" width="63%">
Not implemented in this release.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757380(v=VS.85).aspx">GetStreamPrioritization</a>
</td>
<td align="left" width="63%">
Retrieves the stream prioritization object associated with the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757381(v=VS.85).aspx">RemoveBandwidthSharing</a>
</td>
<td align="left" width="63%">
Removes a bandwidth sharing object from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757382(v=VS.85).aspx">RemoveStreamPrioritization</a>
</td>
<td align="left" width="63%">
Removes a stream prioritization object from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757383(v=VS.85).aspx">SetStorageFormat</a>
</td>
<td align="left" width="63%">
Not implemented in this release.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd757384(v=VS.85).aspx">SetStreamPrioritization</a>
</td>
<td align="left" width="63%">
Assigns a stream prioritization object to the profile.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://msdn.microsoft.com/9dc863da-1842-41e7-b66c-c97e0140046d">Bandwidth Sharing Object</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743298(v=VS.85).aspx">IWMBandwidthSharing Interface</a>



<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757266(v=VS.85).aspx">IWMProfile2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd798573(v=VS.85).aspx">IWMStreamPrioritization Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/cb0345ce-6847-435b-8cbb-f8b93856af9f">Stream Prioritization Object</a>
 

 

