---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataCopier.Open
title: ISpatialAudioMetadataCopier::Open
author: windows-sdk-content
description: Opens an ISpatialAudioMetadataItems object for copying.
old-location: coreaudio\ispatialaudiometadatacopier_open.htm
tech.root: CoreAudio
ms.assetid: F2D077EF-89B0-4BD6-85FB-F0AF63F1986D
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ISpatialAudioMetadataCopier interface [Core Audio],Open method, ISpatialAudioMetadataCopier.Open, ISpatialAudioMetadataCopier::Open, Open, Open method [Core Audio], Open method [Core Audio],ISpatialAudioMetadataCopier interface, coreaudio.ispatialaudiometadatacopier_open, spatialaudiometadata/ISpatialAudioMetadataCopier::Open
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: spatialaudiometadata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - ISpatialAudioMetadataCopier.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioMetadataCopier::Open


## -description


Opens an <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object for copying.


## -parameters




### -param metadataItems [in]

A pointer to an  <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object to be opened for copying


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SPTLAUD_MD_CLNT_E_ITEMS_ALREADY_OPEN</b></dt>
</dl>
</td>
<td width="60%">
<b>Open</b> has already been called on the supplied <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> since the object was created or since the last call to <a href="https://msdn.microsoft.com/891AFF53-7CAB-49FA-A8D2-CAEEB91E860F">Close</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The provided pointer is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/74708744-78BF-4135-BB0A-50A7CA41ECDD">ISpatialAudioMetadataCopier</a>



<a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a>
 

 

