---
UID: NN:wmsdkidl.IWMProfile
title: IWMProfile (wmsdkidl.h)
description: The IWMProfile interface is the primary interface for a profile object.
helpviewer_keywords: ["IWMProfile","IWMProfile interface [windows Media Format]","IWMProfile interface [windows Media Format]","described","IWMProfileInterface","wmformat.iwmprofile","wmsdkidl/IWMProfile"]
old-location: wmformat\iwmprofile.htm
tech.root: wmformat
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
ms.date: 12/05/2018
ms.keywords: IWMProfile, IWMProfile interface [windows Media Format], IWMProfile interface [windows Media Format],described, IWMProfileInterface, wmformat.iwmprofile, wmsdkidl/IWMProfile
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
 - IWMProfile
 - wmsdkidl/IWMProfile
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
 - IWMProfile
---

# IWMProfile interface


## -description

The <b>IWMProfile</b> interface is the primary interface for a <a href="https://docs.microsoft.com/windows/desktop/wmformat/wmformat-glossary">profile</a> object. A profile object is used to configure custom profiles. You can use <b>IWMProfile</b> to create, delete, or modify stream configuration objects and mutual exclusion objects. You can also set and retrieve general information about the profile. To access all the features of the profile object, you should use <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>, which inherits from <b>IWMProfile</b> and <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2">IWMProfile2</a>.

<b>IWMProfile</b> is also accessible through the reader object, where you can use it to get information about the streams of a file that is loaded in the reader. When accessing <b>IWMProfile</b> from the reader, you can make changes to the profile, but none of the changes can be saved to the file. It is often handy to use the profile of an existing file as the foundation of a new profile. The synchronous reader supports <b>IWMProfile</b> in the same way as the reader.

The profile information obtained through the reader or synchronous reader does not come from a .prx file. The reader uses the information in the ASF file to assemble the stream configurations. Thus certain profile information, like the name and description, are not available through the reader.

There are several ways to obtain a pointer to an <b>IWMProfile</b> interface. The profile manager has methods to create a new profile and to access existing profiles. All of these methods set an <b>IWMProfile</b> pointer. When reading a file, a pointer to <b>IWMProfile</b> can be obtained by calling the <b>QueryInterface</b> method of any reader interface. Likewise, any interface of the synchronous reader object can obtain a pointer with a call to <b>QueryInterface</b><a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3">IWMProfile3</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfile</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMProfile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMProfile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion">AddMutualExclusion</a>
</td>
<td align="left" width="63%">
Adds a mutual exclusion object to the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-addstream">AddStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion">CreateNewMutualExclusion</a>
</td>
<td align="left" width="63%">
Creates a mutual exclusion object for the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream">CreateNewStream</a>
</td>
<td align="left" width="63%">
Creates a stream configuration object for the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion">GetMutualExclusion</a>
</td>
<td align="left" width="63%">
Retrieves a mutual exclusion object from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusioncount">GetMutualExclusionCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of mutual exclusion objects in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getname">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Retrieves a stream, using an index number, from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber">GetStreamByNumber</a>
</td>
<td align="left" width="63%">
Retrieves a stream, using the number of the stream, from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of streams in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-getversion">GetVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version number of Microsoft Windows Media Services in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">ReconfigStream</a>
</td>
<td align="left" width="63%">
Enables changes made to a stream configuration to be included in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion">RemoveMutualExclusion</a>
</td>
<td align="left" width="63%">
Removes a mutual exclusion object from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removestream">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a stream from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber">RemoveStreamByNumber</a>
</td>
<td align="left" width="63%">
Removes a stream from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription">SetDescription</a>
</td>
<td align="left" width="63%">
Specifies the description of the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-setname">SetName</a>
</td>
<td align="left" width="63%">
Specifies the name of the profile.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager">IWMProfileManager Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/profile-manager-object">Profile Manager Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/reader-object">Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/synchronous-reader-object">Synchronous Reader Object</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/working-with-profiles">Working with Profiles</a>

