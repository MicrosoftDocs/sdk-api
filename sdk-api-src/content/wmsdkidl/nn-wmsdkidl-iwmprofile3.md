---
UID: NN:wmsdkidl.IWMProfile3
title: IWMProfile3 (wmsdkidl.h)
description: The IWMProfile3 interface provides enhanced features for profiles.
helpviewer_keywords: ["IWMProfile3","IWMProfile3 interface [windows Media Format]","IWMProfile3 interface [windows Media Format]","described","IWMProfile3Interface","wmformat.iwmprofile3","wmsdkidl/IWMProfile3"]
old-location: wmformat\iwmprofile3.htm
tech.root: wmformat
ms.assetid: 7942aa81-ada7-4e9c-a261-f257f8f890b7
ms.date: 12/05/2018
ms.keywords: IWMProfile3, IWMProfile3 interface [windows Media Format], IWMProfile3 interface [windows Media Format],described, IWMProfile3Interface, wmformat.iwmprofile3, wmsdkidl/IWMProfile3
f1_keywords:
- wmsdkidl/IWMProfile3
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMProfile3 interface


## -description



The <b>IWMProfile3</b> interface provides enhanced features for profiles. This includes the ability to create two new types of objects: bandwidth sharing objects and stream prioritization objects.

An <b>IWMProfile3</b> interface is created for each profile object created. You can retrieve a pointer to an <b>IWMProfile3</b> interface by calling the <b>QueryInterface</b> method of any other interface of the profile. You can also access <b>IWMProfile3</b> from a reader or synchronous reader object by calling the <b>QueryInterface</b> method of an existing interface in the object. For more information, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfile3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>. <b>IWMProfile3</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing">AddBandwidthSharing</a>
</td>
<td align="left" width="63%">
Adds an existing bandwidth sharing object to the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing">CreateNewBandwidthSharing</a>
</td>
<td align="left" width="63%">
Creates a new bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewstreamprioritization">CreateNewStreamPrioritization</a>
</td>
<td align="left" width="63%">
Creates a new stream prioritization object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing">GetBandwidthSharing</a>
</td>
<td align="left" width="63%">
Obtains a pointer to the <b>IWMBandwidthSharing</b> interface of an existing bandwidth sharing object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount">GetBandwidthSharingCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of bandwidth sharing objects that exist in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getexpectedpacketcount">GetExpectedPacketCount</a>
</td>
<td align="left" width="63%">
Retrieves the expected number of <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">packets</a> for a specified duration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getstorageformat">GetStorageFormat</a>
</td>
<td align="left" width="63%">
Not implemented in this release.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getstreamprioritization">GetStreamPrioritization</a>
</td>
<td align="left" width="63%">
Retrieves the stream prioritization object associated with the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-removebandwidthsharing">RemoveBandwidthSharing</a>
</td>
<td align="left" width="63%">
Removes a bandwidth sharing object from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-removestreamprioritization">RemoveStreamPrioritization</a>
</td>
<td align="left" width="63%">
Removes a stream prioritization object from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-setstorageformat">SetStorageFormat</a>
</td>
<td align="left" width="63%">
Not implemented in this release.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-setstreamprioritization">SetStreamPrioritization</a>
</td>
<td align="left" width="63%">
Assigns a stream prioritization object to the profile.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/bandwidth-sharing-object">Bandwidth Sharing Object</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing">IWMBandwidthSharing Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/iwmprofile">IWMProfile Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamprioritization">IWMStreamPrioritization Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/stream-prioritization-object">Stream Prioritization Object</a>
 

 

