---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataWriter
title: ISpatialAudioMetadataWriter
author: windows-sdk-content
description: Provides methods for storing spatial audio metadata items positioned within a range of corresponding audio frames.
old-location: coreaudio\ispatialaudiometadatawriter.htm
old-project: CoreAudio
ms.assetid: F8CD8B79-9442-46D0-ABF5-5F6734474B01
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ISpatialAudioMetadataWriter, ISpatialAudioMetadataWriter interface [Core Audio], ISpatialAudioMetadataWriter interface [Core Audio],described, coreaudio.ispatialaudiometadatawriter, spatialaudiometadata/ISpatialAudioMetadataWriter
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spatialaudiometadata.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SpatialAudioMetadata.h
api_name:
 - ISpatialAudioMetadataWriter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioMetadataWriter interface


## -description


Provides methods for storing spatial audio metadata items
positioned within a range of corresponding audio frames.  Each metadata item has a zero-based 
offset position within the specified frame.  Each item can contain one or more commands
specific to the metadata format ID provided in the <a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="https://msdn.microsoft.com/42EDD4D2-3DAA-4F8F-A71C-7EDFEBBCB3FB">ISpatialAudioMetadataClient</a> was created.  
This object does not allocate storage for the metadata it is provided, the caller is expected to manage the allocation of memory used to store the packed data.
Multiple metadata items can be placed in the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object.  For each item, 
call <a href="https://msdn.microsoft.com/9D61BFC0-BAD7-46D3-B0E9-4848E37785E9">WriteNextItem</a> followed by a call to <a href="https://msdn.microsoft.com/A614AEC6-7CA3-4624-BAFE-46618BCB64FA">WriteNextItemCommand</a>.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioMetadataWriter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioMetadataWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioMetadataWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2417E624-6535-49E2-9CF4-F927F731BE41">Close</a>
</td>
<td align="left" width="63%">
Completes any needed operations on the metadata buffer and releases the specified <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49B3401D-7B26-4057-81C0-6C5683B83665">Open</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object for writing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9D61BFC0-BAD7-46D3-B0E9-4848E37785E9">WriteNextItem</a>
</td>
<td align="left" width="63%">
Starts a new metadata item at the specified offset.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A614AEC6-7CA3-4624-BAFE-46618BCB64FA">WriteNextItemCommand</a>
</td>
<td align="left" width="63%">
Writes metadata commands and value data to the current item.

</td>
</tr>
</table> 

