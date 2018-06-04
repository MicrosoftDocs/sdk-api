---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ISpatialAudioMetadataCopier::CopyMetadataForFrames


## -description


Copies metadata items from the source <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a>, provided to the <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> method, object to the destination <b>ISpatialAudioMetadataItems</b> object, specified with the <i>dstMetadataItems</i> parameter.  Each call advances the internal copy position by the number of frames in the <i>copyFrameCount</i> parameter.


## -parameters




### -param copyFrameCount [in]

The number of frames from the current copy position for which metadata items are copied. After the copy, the internal copy position within the source <b>SpatialAudioMetadataItems</b> is advanced the value specified in this parameter. Set this value to 0 to copy the entire frame range contained in the  source <b>SpatialAudioMetadataItems</b>.


### -param copyMode [in]

A value that specifies the copy mode for the operation.


### -param dstMetadataItems [in]

A pointer to the  destination <b>SpatialAudioMetadataItems</b> for the copy operation.


### -param itemsCopied [out]

Receives number of metadata items copied in the operation.


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
The <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> has not been opened for copying with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a> or the object has been closed for writing with a call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the provided pointers is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/74708744-78BF-4135-BB0A-50A7CA41ECDD">ISpatialAudioMetadataCopier</a>
 

 

