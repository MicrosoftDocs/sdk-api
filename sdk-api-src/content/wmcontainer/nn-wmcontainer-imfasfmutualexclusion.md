---
UID: NN:wmcontainer.IMFASFMutualExclusion
title: IMFASFMutualExclusion (wmcontainer.h)
author: windows-sdk-content
description: Configures an Advanced Systems Format (ASF) mutual exclusion object, which manages information about a group of streams in an ASF profile that are mutually exclusive.
old-location: mf\imfasfmutualexclusion.htm
tech.root: medfound
ms.assetid: 9c2278ec-77d1-445e-94bc-44e5d48f14ae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 9c2278ec-77d1-445e-94bc-44e5d48f14ae, IMFASFMutualExclusion, IMFASFMutualExclusion interface [Media Foundation], IMFASFMutualExclusion interface [Media Foundation],described, mf.imfasfmutualexclusion, wmcontainer/IMFASFMutualExclusion
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
 - IMFASFMutualExclusion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFASFMutualExclusion interface


## -description


Configures an Advanced Systems Format (ASF) mutual exclusion object, which manages information about a group of streams in an ASF profile that are mutually exclusive. When streams or groups of streams are mutually exclusive, only one of them is read at a time, they are not read concurrently.

A common example of mutual exclusion is a set of streams that each include the same content encoded at a different bit rate. The stream that is used is determined by the available bandwidth to the reader.

An <b>IMFASFMutualExclusion</b> interface exists for every ASF mutual exclusion object. A pointer to this interface is obtained when you create the object using the <a href="https://msdn.microsoft.com/457b7b73-34c0-48fe-882a-9cdc3516e20d">IMFASFProfile::CreateMutualExclusion</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFASFMutualExclusion</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFASFMutualExclusion</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFASFMutualExclusion</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5dedc87-a29c-4c8d-b493-486d975f9ac4">AddRecord</a>
</td>
<td align="left" width="63%">
Adds a record to the mutual exclusion object. A record specifies streams that are mutually exclusive with the streams in all other records.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfbfe3be-b0a4-408a-952e-e4f996f94cee">AddStreamForRecord</a>
</td>
<td align="left" width="63%">
Adds a stream number to a record in the ASF mutual exclusion object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32bd09d7-9d85-4692-8b2f-6afab3234fa9">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the ASF mutual exclusion object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8dbd883e-4ae3-422d-bb2e-087a9e311558">GetRecordCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of records in the ASF mutual exclusion object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce410ae9-d0d0-4617-8178-829ef3c77ce0">GetStreamsForRecord</a>
</td>
<td align="left" width="63%">
Retrieves the stream numbers contained in a record in the ASF mutual exclusion object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6af870e-2ef8-4dea-b76b-7a78ceaaa3d3">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the type of mutual exclusion represented by the ASF mutual exclusion object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecfb5e10-5102-4f6a-b67b-ba0ed06d0ed8">RemoveRecord</a>
</td>
<td align="left" width="63%">
Removes a record from the ASF mutual exclusion object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d92c022c-3241-4296-9572-62b43c6e79cb">RemoveStreamFromRecord</a>
</td>
<td align="left" width="63%">
Removes a stream number from a record in the ASF mutual exclusion object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58fc1c27-0a7d-48bb-b5a4-ab299c5e0ac6">SetType</a>
</td>
<td align="left" width="63%">
Sets the type of mutual exclusion that is represented by the ASF mutual exclusion object.

</td>
</tr>
</table> 


## -remarks



An ASF profile object can support multiple mutual exclusions. Each must be configured using a separate ASF mutual exclusion object.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/fdd31eac-1dd6-45f0-90fb-d5a74c85db2e">Using Mutual Exclusion for ASF Streams</a>
 

 

