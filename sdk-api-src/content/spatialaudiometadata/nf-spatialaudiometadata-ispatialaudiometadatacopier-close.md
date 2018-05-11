---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataCopier.Close
title: ISpatialAudioMetadataCopier::Close
author: windows-driver-content
description: Completes any necessary operations on the SpatialAudioMetadataItems object and releases the object.
old-location: coreaudio\ispatialaudiometadatacopier_close.htm
old-project: CoreAudio
ms.assetid: 891AFF53-7CAB-49FA-A8D2-CAEEB91E860F
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Close, Close method [Core Audio], Close method [Core Audio],ISpatialAudioMetadataCopier interface, ISpatialAudioMetadataCopier interface [Core Audio],Close method, ISpatialAudioMetadataCopier.Close, ISpatialAudioMetadataCopier::Close, coreaudio.ispatialaudiometadatacopier_close, spatialaudiometadata/ISpatialAudioMetadataCopier::Close
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
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SpatialAudioMetadata.h
api_name:
-	ISpatialAudioMetadataCopier.Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
---

# ISpatialAudioMetadataCopier::Close


## -description


Completes any necessary operations on the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">SpatialAudioMetadataItems</a> object  and releases the object.


## -parameters






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
<dt><b>SPTLAUD_MD_CLNT_E_NO_ITEMS_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> has not been opened for reading with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> or the object has been closed for writing with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/74708744-78BF-4135-BB0A-50A7CA41ECDD">ISpatialAudioMetadataCopier</a>



<a href="https://msdn.microsoft.com/BD1AD4CE-6E88-4292-AA79-E71FE00C2078">ISpatialAudioMetadataReader</a>
 

 

