---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataItems
title: ISpatialAudioMetadataItems (spatialaudiometadata.h)
description: Represents a buffer of spatial audio metadata items.
helpviewer_keywords: ["ISpatialAudioMetadataItems","ISpatialAudioMetadataItems interface [Core Audio]","ISpatialAudioMetadataItems interface [Core Audio]","described","coreaudio.ispatialaudiometadataitems","spatialaudiometadata/ISpatialAudioMetadataItems"]
old-location: coreaudio\ispatialaudiometadataitems.htm
tech.root: CoreAudio
ms.assetid: 54A6B7DE-A41E-4214-AF02-CC19250B9037
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataItems, ISpatialAudioMetadataItems interface [Core Audio], ISpatialAudioMetadataItems interface [Core Audio],described, coreaudio.ispatialaudiometadataitems, spatialaudiometadata/ISpatialAudioMetadataItems
req.header: spatialaudiometadata.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioMetadataItems
 - spatialaudiometadata/ISpatialAudioMetadataItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SpatialAudioMetadata.h
api_name:
 - ISpatialAudioMetadataItems
---

# ISpatialAudioMetadataItems interface


## -description

Represents a buffer of spatial audio metadata items. Metadata commands and values can be written to, read from, and copied between ISpatialAudioMetadataItems using the <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a>, <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatacopier">ISpatialAudioMetadataCopier</a> interfaces. Use caller-allocated memory to store metadata items by creating an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitemsbuffer">ISpatialAudioMetadataItemsBuffer</a>.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioMetadataItems</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioMetadataItems</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataitems-getframecount">GetFrameCount</a>
</td>
<td align="left" width="63%">
Gets the total frame count of the <b>ISpatialAudioMetadataItems</b>, which defines valid item offsets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataitems-getinfo">GetInfo</a>
</td>
<td align="left" width="63%">
Gets the total frame count for the <b>ISpatialAudioMetadataItems</b>, which defines valid item offsets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataitems-getitemcount">GetItemCount</a>
</td>
<td align="left" width="63%">
The current number of items stored by the <b>ISpatialAudioMetadataItems</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataitems-getmaxitemcount">GetMaxItemCount</a>
</td>
<td align="left" width="63%">
The maximum number of items allowed by the <b>ISpatialAudioMetadataItems</b>, defined when the object is created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataitems-getmaxvaluebufferlength">GetMaxValueBufferLength</a>
</td>
<td align="left" width="63%">
The size of the largest command value defined by the metadata format for the <b>ISpatialAudioMetadataItems</b>.

</td>
</tr>
</table>

## -remarks

Get an instance of this interface by calling <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadataitems">ISpatialAudioMetadataClient::ActivateSpatialAudioMetadataItems</a>.

