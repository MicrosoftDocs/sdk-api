---
UID: NN:wmcontainer.IMFASFProfile
title: IMFASFProfile
author: windows-sdk-content
description: Manages an Advanced Systems Format (ASF) profile.
old-location: mf\imfasfprofile.htm
tech.root: medfound
ms.assetid: fe441c61-1be7-4fda-a2a3-bd79ecf4e54c
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFASFProfile, IMFASFProfile interface [Media Foundation], IMFASFProfile interface [Media Foundation],described, fe441c61-1be7-4fda-a2a3-bd79ecf4e54c, mf.imfasfprofile, wmcontainer/IMFASFProfile
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFProfile interface


## -description


Manages an Advanced Systems Format (ASF) profile. A profile is a collection of information that describes the configuration of streams that will be included in an ASF file. Information about the relationships between streams is also included in the profile.

An <b>IMFASFProfile</b> interface exists for every ASF profile object. To create an ASF profile object, call <a href="https://msdn.microsoft.com/fa57fac7-a191-4d5b-89be-319af7b3e09c">MFCreateASFProfile</a> or <a href="https://msdn.microsoft.com/1163d958-fbea-48f3-9ac3-1595c0cc2d32">MFCreateASFProfileFromPresentationDescriptor</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFProfile</b> interface inherits from <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>. <b>IMFASFProfile</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d9069feb-7d39-4b40-b95e-0112d959bbae">AddMutualExclusion</a>
</td>
<td align="left" width="63%">
Adds a configured ASF mutual exclusion object to the profile.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64bbe28b-c167-4734-8ceb-5a36da4a0c70">AddStreamPrioritization</a>
</td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e91d3d2c-ef08-460e-b6f8-e8eed8df5a67">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the ASF profile object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/457b7b73-34c0-48fe-882a-9cdc3516e20d">CreateMutualExclusion</a>
</td>
<td align="left" width="63%">
Creates a new ASF mutual exclusion object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3da52c1a-24c0-456b-a9e8-57b5467eda2a">CreateStream</a>
</td>
<td align="left" width="63%">
Creates an ASF stream configuration object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c3a5470-eba9-4233-8744-8630002d3fa0">CreateStreamPrioritization</a>
</td>
<td align="left" width="63%">
Not implemented.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b9e37fc-0bd8-4502-9e90-76330a08f68b">GetMutualExclusion</a>
</td>
<td align="left" width="63%">
Retrieves an ASF mutual exclusion object from the profile.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e275b83-9e59-4730-b8e2-e45f78077891">GetMutualExclusionCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of ASF mutual exclusion objects that are associated with the profile.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/918f6534-811e-42f6-9836-1c77816007fa">GetStream</a>
</td>
<td align="left" width="63%">
Retrieves a stream from the profile by stream index, and/or retrieves the stream number for a stream index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e3fadf0-1549-4d51-b263-727b15c55023">GetStreamByNumber</a>
</td>
<td align="left" width="63%">
Retrieves an ASF stream configuration object for a stream in the profile. This method references the stream by stream number instead of stream index.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf8c6157-3420-4097-8ab6-f307a69d418a">GetStreamCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of streams in the profile.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/28c542b9-a121-4002-83ae-d6dcfa6f0b6a">GetStreamPrioritization</a>
</td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dbcf192f-1ab4-44c4-8444-5d2aba941fe1">RemoveMutualExclusion</a>
</td>
<td align="left" width="63%">
Removes an ASF mutual exclusion object from the profile.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfe404d3-66ea-407b-a2e0-caa065f41afe">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a stream from the ASF profile object.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6076091-ab38-4722-bb95-fac253e26c8a">RemoveStreamPrioritization</a>
</td>
<td align="left" width="63%">
Not supported.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2272260-74ab-42ff-bff3-d6c6d5b322f3">SetStream</a>
</td>
<td align="left" width="63%">
Adds a stream to the profile or reconfigures an existing stream.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/03a0981b-29c3-450d-aa58-bc56a76e6cb6">ASF Profile</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

