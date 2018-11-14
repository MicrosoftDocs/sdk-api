---
UID: NN:wmsdkidl.IWMMutualExclusion2
title: IWMMutualExclusion2
author: windows-sdk-content
description: The IWMMutualExclusion2 interface provides advanced configuration features for mutual exclusion objects.This interface supports both multiple languages and advanced mutual exclusion.An IWMMutualExclusion2 interface is created for each mutual exclusion object created. To retrieve a pointer to an IWMMutualExclusion2 interface, call the QueryInterface method of the IWMMutualExclusion interface returned by IWMProfile::CreateNewMutualExclusion.
old-location: wmformat\iwmmutualexclusion2.htm
tech.root: wmformat
ms.assetid: 4a1f468c-2ba5-48a1-b56f-8b62aacf1ccf
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMMutualExclusion2, IWMMutualExclusion2 interface [windows Media Format], IWMMutualExclusion2 interface [windows Media Format],described, IWMMutualExclusion2Interface, wmformat.iwmmutualexclusion2, wmsdkidl/IWMMutualExclusion2
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMMutualExclusion2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMMutualExclusion2 interface


## -description



The <b>IWMMutualExclusion2</b> interface provides advanced configuration features for mutual exclusion objects.

This interface supports both multiple languages and advanced mutual exclusion.

An <b>IWMMutualExclusion2</b> interface is created for each mutual exclusion object created. To retrieve a pointer to an <b>IWMMutualExclusion2</b> interface, call the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/040635fb-de00-4c8c-9c39-c28c409311c3">IWMMutualExclusion</a> interface returned by <a href="https://msdn.microsoft.com/fcf3a549-5ae1-459a-95b9-923570f59a4a">IWMProfile::CreateNewMutualExclusion</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMMutualExclusion2</b> interface inherits from <a href="https://msdn.microsoft.com/040635fb-de00-4c8c-9c39-c28c409311c3">IWMMutualExclusion</a>. <b>IWMMutualExclusion2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMMutualExclusion2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58eaa4b2-65d3-44b1-8e3d-1aac01057d0f">AddRecord</a>
</td>
<td align="left" width="63%">
Adds a record to the mutual exclusion object. Records can hold groups of streams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/501fae9f-84b3-4025-83bc-ad0bbe47384d">AddStreamForRecord</a>
</td>
<td align="left" width="63%">
Adds a stream to the list in a record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da62ed2e-7356-4b4e-b2c5-6c18ef806ba7">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name that has been assigned to the mutual exclusion object through a call to <b>SetName</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e113601-1ac7-42a3-8e46-f1ba67ebb071">GetRecordCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of records that exist for the mutual exclusion object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7508a473-77ae-49ce-b041-2d171193e730">GetRecordName</a>
</td>
<td align="left" width="63%">
Retrieves the name that has been assigned to a record through a call to <b>SetName</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a94a64e9-96c6-4aba-a5b4-f50d14c19b73">GetStreamsForRecord</a>
</td>
<td align="left" width="63%">
Retrieves the list of all streams in a record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74e2825e-2200-4750-bb16-f8cf9f80ab7e">RemoveRecord</a>
</td>
<td align="left" width="63%">
Removes a record from the mutual exclusion object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a32d78b7-47a3-45b6-9575-c290adf86094">RemoveStreamForRecord</a>
</td>
<td align="left" width="63%">
Removes a stream from the list in a record.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b288c28c-04bd-49a4-bf11-21d4968772d4">SetName</a>
</td>
<td align="left" width="63%">
Assigns a name to the mutual exclusion object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9527024e-2d52-4a81-90a5-4ef5241ba6dd">SetRecordName</a>
</td>
<td align="left" width="63%">
Assigns a name to a record.

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
<a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList</a>
</td>
<td>IID_IWMStreamList</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/040635fb-de00-4c8c-9c39-c28c409311c3">IWMMutualExclusion</a>
</td>
<td>IID_IWMMutualExclusion</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/040635fb-de00-4c8c-9c39-c28c409311c3">IWMMutualExclusion Interface</a>



<a href="https://msdn.microsoft.com/dd1f7865-e409-4bf9-9fa0-769a29eaed60">Mutual Exclusion Object</a>
 

 

