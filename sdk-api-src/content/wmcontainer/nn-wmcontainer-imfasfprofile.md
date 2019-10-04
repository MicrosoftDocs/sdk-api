---
UID: NN:wmcontainer.IMFASFProfile
title: IMFASFProfile (wmcontainer.h)
author: windows-sdk-content
description: Manages an Advanced Systems Format (ASF) profile.
old-location: mf\imfasfprofile.htm
tech.root: medfound
ms.assetid: fe441c61-1be7-4fda-a2a3-bd79ecf4e54c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFASFProfile, IMFASFProfile interface [Media Foundation], IMFASFProfile interface [Media Foundation],described, fe441c61-1be7-4fda-a2a3-bd79ecf4e54c, mf.imfasfprofile, wmcontainer/IMFASFProfile
ms.topic: interface
f1_keywords: 
 - "wmcontainer/IMFASFProfile"
dev_langs:
 - c++
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFProfile
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFASFProfile interface


## -description


Manages an Advanced Systems Format (ASF) profile. A profile is a collection of information that describes the configuration of streams that will be included in an ASF file. Information about the relationships between streams is also included in the profile.

An <b>IMFASFProfile</b> interface exists for every ASF profile object. To create an ASF profile object, call <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile">MFCreateASFProfile</a> or <a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor">MFCreateASFProfileFromPresentationDescriptor</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFProfile</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>. <b>IMFASFProfile</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFProfile</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion">AddMutualExclusion</a>
</td>
<td align="left" width="63%">
Adds a configured ASF mutual exclusion object to the profile.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addstreamprioritization">AddStreamPrioritization</a>
</td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the ASF profile object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion">CreateMutualExclusion</a>
</td>
<td align="left" width="63%">
Creates a new ASF mutual exclusion object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream">CreateStream</a>
</td>
<td align="left" width="63%">
Creates an ASF stream configuration object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstreamprioritization">CreateStreamPrioritization</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion">GetMutualExclusion</a>
</td>
<td align="left" width="63%">
Retrieves an ASF mutual exclusion object from the profile.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount">GetMutualExclusionCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of ASF mutual exclusion objects that are associated with the profile.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream">GetStream</a>
</td>
<td align="left" width="63%">
Retrieves a stream from the profile by stream index, and/or retrieves the stream number for a stream index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber">GetStreamByNumber</a>
</td>
<td align="left" width="63%">
Retrieves an ASF stream configuration object for a stream in the profile. This method references the stream by stream number instead of stream index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of streams in the profile.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamprioritization">GetStreamPrioritization</a>
</td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion">RemoveMutualExclusion</a>
</td>
<td align="left" width="63%">
Removes an ASF mutual exclusion object from the profile.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a stream from the ASF profile object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestreamprioritization">RemoveStreamPrioritization</a>
</td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream">SetStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the profile or reconfigures an existing stream.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/asf-profile">ASF Profile</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

