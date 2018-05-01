---
UID: NF:mfspatialaudio.IMFSpatialAudioObjectBuffer.GetMetadataItems
title: IMFSpatialAudioObjectBuffer::GetMetadataItems method
author: windows-driver-content
description: Retrieves a pointer to a buffer that may contain spatial audio metadata.
old-location: mf\imfspatialaudioobjectbuffer_getmetadataitems.htm
old-project: medfound
ms.assetid: 19BF7AC6-B21F-47D1-8573-48C5E4869574
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: GetMetadataItems method [Media Foundation], GetMetadataItems method [Media Foundation], IMFSpatialAudioObjectBuffer interface, GetMetadataItems,IMFSpatialAudioObjectBuffer.GetMetadataItems, IMFSpatialAudioObjectBuffer, IMFSpatialAudioObjectBuffer interface [Media Foundation], GetMetadataItems method, IMFSpatialAudioObjectBuffer::GetMetadataItems, mf.imfspatialaudioobjectbuffer_getmetadataitems, mfspatialaudio/IMFSpatialAudioObjectBuffer::GetMetadataItems
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfspatialaudio.h
req.include-header: Mfobjects.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: DEVICE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfobjects.lib
-	mfobjects.dll
api_name:
-	IMFSpatialAudioObjectBuffer.GetMetadataItems
product: Windows
targetos: Windows
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFSpatialAudioObjectBuffer::GetMetadataItems method


## -description


Retrieves a pointer to a buffer that may 
    contain spatial audio metadata.  


## -parameters




### -param ppMetadataItems [out]

A pointer to an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object in which the collection
    of metadata items will be stored.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The supplied pointer is invalid.

</td>
</tr>
</table>
 




## -remarks



The metadata is written to the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a>
    collection in a format identified by the <a href="https://msdn.microsoft.com/9714A2C7-25A1-4735-A0AC-22329ECBBC46">MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID</a>     media type attribute specified during media type negotiation phase of Media Foundation     topology construction.




## -see-also




<a href="https://msdn.microsoft.com/61E9BC6A-2120-4874-9053-E1D232DF1CCA">IMFSpatialAudioObjectBuffer</a>
 

 

