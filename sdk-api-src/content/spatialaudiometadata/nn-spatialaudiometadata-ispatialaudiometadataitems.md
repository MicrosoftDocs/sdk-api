---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataItems
title: ISpatialAudioMetadataItems
author: windows-sdk-content
description: Represents a buffer of spatial audio metadata items.
old-location: coreaudio\ispatialaudiometadataitems.htm
old-project: CoreAudio
ms.assetid: 54A6B7DE-A41E-4214-AF02-CC19250B9037
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: ISpatialAudioMetadataItems, ISpatialAudioMetadataItems interface [Core Audio], ISpatialAudioMetadataItems interface [Core Audio],described, coreaudio.ispatialaudiometadataitems, spatialaudiometadata/ISpatialAudioMetadataItems
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
 - ISpatialAudioMetadataItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioMetadataItems interface


## -description


Represents a buffer of spatial audio metadata items. Metadata commands and values can be written to, read from, and copied between ISpatialAudioMetadataItems using the <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a>, <a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a>, and <a href="https://msdn.microsoft.com/74708744-78BF-4135-BB0A-50A7CA41ECDD">ISpatialAudioMetadataCopier</a> interfaces. Use caller-allocated memory to store metadata items by creating an <a href="https://msdn.microsoft.com/5DDD468E-0C46-4C00-BCFF-1FF7353ADB8B">ISpatialAudioMetadataItemsBuffer</a>.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioMetadataItems</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioMetadataItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioMetadataItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5932E338-AB0E-4D1E-9B7E-36E2D5A76B18">GetFrameCount</a>
</td>
<td align="left" width="63%">
Gets the total frame count of the <b>ISpatialAudioMetadataItems</b>, which defines valid item offsets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F54BF2B9-B9A4-47EF-8C18-DC58B24B617E">GetInfo</a>
</td>
<td align="left" width="63%">
Gets the total frame count for the <b>ISpatialAudioMetadataItems</b>, which defines valid item offsets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/168FDDA7-FB87-47B3-A7BC-88398663A7DD">GetItemCount</a>
</td>
<td align="left" width="63%">
The current number of items stored by the <b>ISpatialAudioMetadataItems</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/933DEDE0-3DC1-4D0B-8EAE-58EFB52CE2FE">GetMaxItemCount</a>
</td>
<td align="left" width="63%">
The maximum number of items allowed by the <b>ISpatialAudioMetadataItems</b>, defined when the object is created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B6D4117B-CDFE-49E8-A9BC-B69AEBA7C9AC">GetMaxValueBufferLength</a>
</td>
<td align="left" width="63%">
The size of the largest command value defined by the metadata format for the <b>ISpatialAudioMetadataItems</b>.

</td>
</tr>
</table> 


## -remarks



Get an instance of this interface by calling <a href="https://msdn.microsoft.com/0788C3BE-1616-4C7B-8F47-B0C4E4034061">ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems</a>.



