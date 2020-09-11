---
UID: NN:wmsdkidl.IWMMutualExclusion
title: IWMMutualExclusion (wmsdkidl.h)
description: The IWMMutualExclusion interface represents a group of streams, of which only one at a time can be played.IWMMutualExclusion is the base interface for mutual exclusion objects.
helpviewer_keywords: ["IWMMutualExclusion","IWMMutualExclusion interface [windows Media Format]","IWMMutualExclusion interface [windows Media Format]","described","IWMMutualExclusionInterface","wmformat.iwmmutualexclusion","wmsdkidl/IWMMutualExclusion"]
old-location: wmformat\iwmmutualexclusion.htm
tech.root: wmformat
ms.assetid: 040635fb-de00-4c8c-9c39-c28c409311c3
ms.date: 12/05/2018
ms.keywords: IWMMutualExclusion, IWMMutualExclusion interface [windows Media Format], IWMMutualExclusion interface [windows Media Format],described, IWMMutualExclusionInterface, wmformat.iwmmutualexclusion, wmsdkidl/IWMMutualExclusion
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMMutualExclusion
 - wmsdkidl/IWMMutualExclusion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMMutualExclusion
---

# IWMMutualExclusion interface


## -description

The <b>IWMMutualExclusion</b> interface represents a group of streams, of which only one at a time can be played.

<b>IWMMutualExclusion</b> is the base interface for mutual exclusion objects. You can create a mutual exclusion object only as part of a profile. Never use COM functions, such as <b>CoCreateInstance</b>, to create a mutual exclusion object. Instead, you must already have a profile opened and make a call to its <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion">IWMProfile::CreateNewMutualExclusion</a> method. After a mutual exclusion object has been created, you can change the type of mutual exclusion by using the methods in this interface.

You can manage the streams in a mutual exclusion object using the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a> interface. <b>IWMMutualExclusion</b> inherits from <b>IWMStreamList</b>, so those methods are directly available in this interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMMutualExclusion</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a>. <b>IWMMutualExclusion</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMMutualExclusion</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the type of mutual exclusion required.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype">SetType</a>
</td>
<td align="left" width="63%">
Specifies the GUID of the type of mutual exclusion required.

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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a>
</td>
<td>IID_IWMStreamList</td>
</tr>
<tr>
<td>
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2">IWMMutualExclusion2</a>
</td>
<td>IID_IWMMutualExclusion2</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist">IWMStreamList</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>

