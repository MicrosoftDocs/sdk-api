---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataReader
title: ISpatialAudioMetadataReader
author: windows-sdk-content
description: Provides methods for extracting spatial audio metadata items and item command value pairs from an ISpatialAudioMetadataItems object.
old-location: coreaudio\ispatialaudiometadatareader.htm
tech.root: CoreAudio
ms.assetid: BD1AD4CE-6E88-4292-AA79-E71FE00C2078
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISpatialAudioMetadataReader, ISpatialAudioMetadataReader interface [Core Audio], ISpatialAudioMetadataReader interface [Core Audio],described, coreaudio.ispatialaudiometadatareader, spatialaudiometadata/ISpatialAudioMetadataReader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SpatialAudioMetadata.h
api_name:
 - ISpatialAudioMetadataReader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioMetadataReader interface


## -description


Provides methods for extracting
spatial audio metadata items and item command value pairs from an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object.
The <b>SpatialAudioMetadataItems</b> object, which is populated using an  <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> or <a href="https://msdn.microsoft.com/74708744-78BF-4135-BB0A-50A7CA41ECDD">ISpatialAudioMetadataCopier</a>, has a frame count, specified with the <i>frameCount</i> parameter to <a href="https://msdn.microsoft.com/0788C3BE-1616-4C7B-8F47-B0C4E4034061">ActivateSpatialAudioMetadataItems</a>,
that represents the valid range of metadata item offsets.  <b>ISpatialAudioMetadataReader</b> enables reading back
groups of items within a subrange of the total frame count.  The object
maintains an internal read position, which is advanced by the number of frames specified when read operation is performed.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioMetadataReader</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioMetadataReader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioMetadataReader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A9E878E8-A319-4DB3-86A7-4499EDA567F7">Close</a>
</td>
<td align="left" width="63%">
Completes any necessary operations on the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">SpatialAudioMetadataItems</a> object  and releases the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50007A27-D885-47F6-9D3A-1F5B6D47BCDD">Open</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object for reading.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E9958586-0B1E-4864-AE0F-A9805114A797">ReadItemCountinFrames</a>
</td>
<td align="left" width="63%">
Specifies the range, in frames, from which the caller wishes to extract metadata items from the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object.  This method returns the number of metadata items present in the specified range of frames. Each call advances the internal copy position by the number of frames in the <i>readFrameCount</i> parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC1D5FD6-EFF1-410F-95C7-B13EACBED5D1">ReadNextItem</a>
</td>
<td align="left" width="63%">
Gets the number of commands and the sample offset for the metadata item being read.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9B58546A-FBE3-47CD-8E5F-63D0C5608F00">ReadNextItemCommand</a>
</td>
<td align="left" width="63%">
Reads metadata commands and value data for the current item.

</td>
</tr>
</table> 

