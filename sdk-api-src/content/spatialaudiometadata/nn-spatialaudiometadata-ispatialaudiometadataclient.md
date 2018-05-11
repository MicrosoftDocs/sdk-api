---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataClient
title: ISpatialAudioMetadataClient
author: windows-driver-content
description: Provides a class factory for creating ISpatialAudioMetadataItems, ISpatialAudioMetadataWriter, ISpatialAudioMetadataReader, and ISpatialAudioMetadataCopier objects.
old-location: coreaudio\ispatialaudiometadataclient.htm
old-project: CoreAudio
ms.assetid: 42EDD4D2-3DAA-4F8F-A71C-7EDFEBBCB3FB
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ISpatialAudioMetadataClient, ISpatialAudioMetadataClient interface [Core Audio], ISpatialAudioMetadataClient interface [Core Audio],described, coreaudio.ispatialaudiometadataclient, spatialaudiometadata/ISpatialAudioMetadataClient
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
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SpatialAudioMetadata.h
api_name:
-	ISpatialAudioMetadataClient
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ISpatialAudioMetadataClient interface


## -description



Provides a class factory for creating
<a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a>, <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a>, <a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a>, and <a href="https://msdn.microsoft.com/74708744-78BF-4135-BB0A-50A7CA41ECDD">ISpatialAudioMetadataCopier</a> objects.
When an <b>ISpatialAudioMetadataItems</b> is activated, a metadata format  ID is specified,     which defines the metadata format enforced for all objects created from this factory.
If the specified format is not supported by the current audio render endpoint, the class factory will not successfully activate the interface and will return an error.



This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioMetadataClient</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISpatialAudioMetadataClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioMetadataClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52534220-65A0-46BE-9A05-E00B84170382">ActivateSpatialAudioMetadataCopier</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> object for copying spatial audio metadata items from one <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0788C3BE-1616-4C7B-8F47-B0C4E4034061">ActivateSpatialAudioMetadataItems</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object for storing spatial audio metadata items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3A49BB96-275A-4886-A45E-42FA7B9A6B5F">ActivateSpatialAudioMetadataReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> object for reading spatial audio metadata items from an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0A30C838-E9B0-4CC3-BE88-9354160B8084">ActivateSpatialAudioMetadataWriter</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://msdn.microsoft.com/F8CD8B79-9442-46D0-ABF5-5F6734474B01">ISpatialAudioMetadataWriter</a> object for writing spatial audio metadata items to an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63D23390-222C-4F7E-AF8A-B49C85DFB222">GetSpatialAudioMetadataItemsBufferLength</a>
</td>
<td align="left" width="63%">
Gets the length of the buffer required to store the specified number of spatial audio metadata items. Use this method to determine the correct buffer size to use when attaching caller-provided memory through the <a href="https://msdn.microsoft.com/5DDD468E-0C46-4C00-BCFF-1FF7353ADB8B">ISpatialAudioMetadataItemsBuffer</a> interface.

</td>
</tr>
</table> 

