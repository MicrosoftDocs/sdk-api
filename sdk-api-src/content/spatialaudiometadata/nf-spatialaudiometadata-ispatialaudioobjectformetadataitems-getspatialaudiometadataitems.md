---
UID: NF:spatialaudiometadata.ISpatialAudioObjectForMetadataItems.GetSpatialAudioMetadataItems
title: ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems
author: windows-sdk-content
description: Gets a pointer to the ISpatialAudioMetadataItems object which stores metadata items for the ISpatialAudioObjectForMetadataItems.
old-location: coreaudio\ispatialaudioobjectformetadataitems_getspatialaudiometadataitems.htm
old-project: CoreAudio
ms.assetid: FD356AA9-F4BC-4864-8A9F-994EB527E123
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetSpatialAudioMetadataItems, GetSpatialAudioMetadataItems method [Core Audio], GetSpatialAudioMetadataItems method [Core Audio],ISpatialAudioObjectForMetadataItems interface, ISpatialAudioObjectForMetadataItems interface [Core Audio],GetSpatialAudioMetadataItems method, ISpatialAudioObjectForMetadataItems.GetSpatialAudioMetadataItems, ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems, coreaudio.ispatialaudioobjectformetadataitems_getspatialaudiometadataitems, spatialaudiometadata/ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: spatialaudiometadata.h
req.include-header: Spatialaudioclient.h
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
tech.root: 
req.typenames: SpatialAudioMetadataWriterOverflowMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	spatialaudiometadata.h
api_name:
-	ISpatialAudioObjectForMetadataItems.GetSpatialAudioMetadataItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISpatialAudioObjectForMetadataItems::GetSpatialAudioMetadataItems


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object which stores metadata items for  the  <a href="https://msdn.microsoft.com/4861D2AA-E685-4A72-BE98-6FEEB72ACF67">ISpatialAudioObjectForMetadataItems</a>.


## -parameters




### -param metadataItems [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> associated with the <a href="https://msdn.microsoft.com/4861D2AA-E685-4A72-BE98-6FEEB72ACF67">ISpatialAudioObjectForMetadataItems</a>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The supplied pointer is invalid.

</td>
</tr>
</table>
 




## -remarks



The client must free this object when it is no longer being used by calling <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>.




## -see-also




<a href="https://msdn.microsoft.com/4861D2AA-E685-4A72-BE98-6FEEB72ACF67">ISpatialAudioObjectForMetadataItems</a>
 

 

