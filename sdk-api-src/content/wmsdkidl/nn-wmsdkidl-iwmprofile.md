---
UID: NN:wmsdkidl.IWMProfile
title: IWMProfile
author: windows-sdk-content
description: The IWMProfile interface is the primary interface for a profile object.
old-location: wmformat\iwmprofile.htm
tech.root: wmformat
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMProfile, IWMProfile interface [windows Media Format], IWMProfile interface [windows Media Format],described, IWMProfileInterface, wmformat.iwmprofile, wmsdkidl/IWMProfile
ms.prod: windows
ms.technology: windows-sdk
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
 - IWMProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfile interface


## -description



The <b>IWMProfile</b> interface is the primary interface for a <a href="wmformat_glossary.htm">profile</a> object. A profile object is used to configure custom profiles. You can use <b>IWMProfile</b> to create, delete, or modify stream configuration objects and mutual exclusion objects. You can also set and retrieve general information about the profile. To access all the features of the profile object, you should use <a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>, which inherits from <b>IWMProfile</b> and <a href="https://msdn.microsoft.com/34e30edb-3247-4eaa-9a63-6d94c9e37c0b">IWMProfile2</a>.

<b>IWMProfile</b> is also accessible through the reader object, where you can use it to get information about the streams of a file that is loaded in the reader. When accessing <b>IWMProfile</b> from the reader, you can make changes to the profile, but none of the changes can be saved to the file. It is often handy to use the profile of an existing file as the foundation of a new profile. The synchronous reader supports <b>IWMProfile</b> in the same way as the reader.

The profile information obtained through the reader or synchronous reader does not come from a .prx file. The reader uses the information in the ASF file to assemble the stream configurations. Thus certain profile information, like the name and description, are not available through the reader.

There are several ways to obtain a pointer to an <b>IWMProfile</b> interface. The profile manager has methods to create a new profile and to access existing profiles. All of these methods set an <b>IWMProfile</b> pointer. When reading a file, a pointer to <b>IWMProfile</b> can be obtained by calling the <b>QueryInterface</b> method of any reader interface. Likewise, any interface of the synchronous reader object can obtain a pointer with a call to <b>QueryInterface</b><a href="https://msdn.microsoft.com/7942aa81-ada7-4e9c-a261-f257f8f890b7">IWMProfile3</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfile</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMProfile</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/efd751cf-d34d-4e74-9a00-444ec31ebef0">AddMutualExclusion</a>
</td>
<td align="left" width="63%">
Adds a mutual exclusion object to the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3024fd2b-c261-49bd-b9a7-c1f43b31645b">AddStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcf3a549-5ae1-459a-95b9-923570f59a4a">CreateNewMutualExclusion</a>
</td>
<td align="left" width="63%">
Creates a mutual exclusion object for the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a1478ff-00fb-46e2-97a3-e00e9c1b819a">CreateNewStream</a>
</td>
<td align="left" width="63%">
Creates a stream configuration object for the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa680ddb-091b-4461-8979-9330f8d59cea">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description of the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/949bb57f-8656-420e-b317-8ca7eb977a4e">GetMutualExclusion</a>
</td>
<td align="left" width="63%">
Retrieves a mutual exclusion object from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c223f75b-87c6-49bd-a16a-14b4751d5f1b">GetMutualExclusionCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of mutual exclusion objects in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5993e47-842d-4392-9b54-2bf6f09c377c">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/067c3f03-a79a-4693-b963-7081f79c72d3">GetStream</a>
</td>
<td align="left" width="63%">
Retrieves a stream, using an index number, from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/507b1c55-1ecb-41dd-a6e5-298e1047a7ea">GetStreamByNumber</a>
</td>
<td align="left" width="63%">
Retrieves a stream, using the number of the stream, from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49534bc3-9115-422b-b448-b6f9c6ec1c47">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of streams in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f74378e-4b60-4b49-8107-26eebdfab02a">GetVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version number of Microsoft Windows Media Services in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">ReconfigStream</a>
</td>
<td align="left" width="63%">
Enables changes made to a stream configuration to be included in the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eb453285-a4e5-48dd-a4d0-72d2e09badc2">RemoveMutualExclusion</a>
</td>
<td align="left" width="63%">
Removes a mutual exclusion object from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82817b72-fde5-492e-b197-87bf145d0be9">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a stream from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72ecc794-d393-416e-bc21-5a7756e76d99">RemoveStreamByNumber</a>
</td>
<td align="left" width="63%">
Removes a stream from the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79ff6ba8-b94b-4c06-a7a5-18b6a8ebc222">SetDescription</a>
</td>
<td align="left" width="63%">
Specifies the description of the profile.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4b38ec1-8fd8-4bfe-8513-33132379f6da">SetName</a>
</td>
<td align="left" width="63%">
Specifies the name of the profile.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>



<a href="https://msdn.microsoft.com/b5edbf8b-820f-4e09-a482-8efc2283360e">Reader Object</a>



<a href="https://msdn.microsoft.com/52a4891f-03bf-4d8a-ab7b-e9739db30bc3">Synchronous Reader Object</a>



<a href="https://msdn.microsoft.com/e1e31632-0db7-47db-a992-f5db9d8824c1">Working with Profiles</a>
 

 

