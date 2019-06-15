---
UID: NF:spatialaudiometadata.ISpatialAudioMetadataCopier.Close
title: ISpatialAudioMetadataCopier::Close (spatialaudiometadata.h)
author: windows-sdk-content
description: Completes any necessary operations on the SpatialAudioMetadataItems object and releases the object.
old-location: coreaudio\ispatialaudiometadatacopier_close.htm
tech.root: CoreAudio
ms.assetid: 891AFF53-7CAB-49FA-A8D2-CAEEB91E860F
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Close, Close method [Core Audio], Close method [Core Audio],ISpatialAudioMetadataCopier interface, ISpatialAudioMetadataCopier interface [Core Audio],Close method, ISpatialAudioMetadataCopier.Close, ISpatialAudioMetadataCopier::Close, coreaudio.ispatialaudiometadatacopier_close, spatialaudiometadata/ISpatialAudioMetadataCopier::Close
ms.topic: method
f1_keywords: ["spatialaudiometadata/ISpatialAudioMetadataCopier.Close"]
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
 - ISpatialAudioMetadataCopier.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpatialAudioMetadataCopier::Close


## -description


Completes any necessary operations on the <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">SpatialAudioMetadataItems</a> object  and releases the object.


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
The <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> has not been opened for reading with a call to <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatareader-open">Open</a> or the object has been closed for writing with a call to <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadatareader-close">Close</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatacopier">ISpatialAudioMetadataCopier</a>



<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>
 

 

