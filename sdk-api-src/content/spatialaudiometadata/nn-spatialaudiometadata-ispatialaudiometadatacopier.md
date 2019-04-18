---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataCopier
title: ISpatialAudioMetadataCopier (spatialaudiometadata.h)
author: windows-sdk-content
description: Provides methods for copying all or subsets of metadata items from a source SpatialAudioMetadataItems into a destination SpatialAudioMetadataItems.
old-location: coreaudio\ispatialaudiometadatacopier.htm
tech.root: CoreAudio
ms.assetid: 74708744-78BF-4135-BB0A-50A7CA41ECDD
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataCopier, ISpatialAudioMetadataCopier interface [Core Audio], ISpatialAudioMetadataCopier interface [Core Audio],described, coreaudio.ispatialaudiometadatacopier, spatialaudiometadata/ISpatialAudioMetadataCopier
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
 - ISpatialAudioMetadataCopier
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpatialAudioMetadataCopier interface


## -description


Provides methods for copying all or subsets of metadata items from a source <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">SpatialAudioMetadataItems</a> into a destination <b>SpatialAudioMetadataItems</b>.
The <b>SpatialAudioMetadataItems</b> object, which is populated using an  <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> or <b>ISpatialAudioMetadataCopier</b>, has a frame count, specified with the <i>frameCount</i> parameter to <a href="https://msdn.microsoft.com/0788C3BE-1616-4C7B-8F47-B0C4E4034061">ActivateSpatialAudioMetadataItems</a>,
that represents the valid range of metadata item offsets.  <b>ISpatialAudioMetadataReader</b> enables copying
groups of items within a subrange of the total frame count.  The object
maintains an internal read position, which is advanced by the number of frames specified when a copy operation is performed.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioMetadataCopier</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioMetadataCopier</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioMetadataCopier</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/891AFF53-7CAB-49FA-A8D2-CAEEB91E860F">Close</a>
</td>
<td align="left" width="63%">
Completes any necessary operations on the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">SpatialAudioMetadataItems</a> object  and releases the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12ABAD23-7EDF-4F74-AE2E-26C75FA6AB37">CopyMetadataForFrames</a>
</td>
<td align="left" width="63%">
Copies metadata items from the source <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a>, provided to the <a href="https://msdn.microsoft.com/F2D077EF-89B0-4BD6-85FB-F0AF63F1986D">Open</a> method, object to the destination <b>ISpatialAudioMetadataItems</b> object, specified with the <i>dstMetadataItems</i> parameter.  Each call advances the internal copy position by the number of frames in the <i>copyFrameCount</i> parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F2D077EF-89B0-4BD6-85FB-F0AF63F1986D">Open</a>
</td>
<td align="left" width="63%">
Opens an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object for copying.

</td>
</tr>
</table> 

