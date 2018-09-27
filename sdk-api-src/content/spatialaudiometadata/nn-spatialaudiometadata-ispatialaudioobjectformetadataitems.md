---
UID: NN:spatialaudiometadata.ISpatialAudioObjectForMetadataItems
title: ISpatialAudioObjectForMetadataItems
author: windows-sdk-content
description: Used to write spatial audio metadata for applications that require multiple metadata items per buffer with frame-accurate placement.
old-location: coreaudio\ispatialaudioobjectformetadataitems.htm
tech.root: CoreAudio
ms.assetid: 4861D2AA-E685-4A72-BE98-6FEEB72ACF67
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ISpatialAudioObjectForMetadataItems, ISpatialAudioObjectForMetadataItems interface [Core Audio], ISpatialAudioObjectForMetadataItems interface [Core Audio],described, coreaudio.ispatialaudioobjectformetadataitems, spatialaudiometadata/ISpatialAudioObjectForMetadataItems
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: spatialaudiometadata.h
req.include-header: Spatialaudioclient.h
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
 - spatialaudiometadata.h
api_name:
 - ISpatialAudioObjectForMetadataItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISpatialAudioObjectForMetadataItems interface


## -description


 Used to write spatial audio metadata for applications that require multiple metadata items per buffer with frame-accurate placement.  The data written via this interface must adhere to the format defined by the metadata format specified in the <a href="https://msdn.microsoft.com/5B92F521-537F-4296-B9A7-7EC6985530B3">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="https://msdn.microsoft.com/1623B280-FC12-4C19-9D4A-D8463D1A1046">ISpatialAudioObjectRenderStreamForMetadata</a> was created.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectForMetadataItems</b> interface inherits from <a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a>. <b>ISpatialAudioObjectForMetadataItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectForMetadataItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6EB7A7B7-6B52-4EB0-81CB-0F9626761CA8">ActivateSpatialAudioObjectForMetadataCommands</a>
</td>
<td align="left" width="63%">
Activate an <a href="https://msdn.microsoft.com/B142D5CC-7321-4F3C-804D-50E728C37D10">ISpatialAudioObjectForMetadataCommands</a> for rendering. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A9743D42-659A-404C-BB21-8A5086870F34">ActivateSpatialAudioObjectForMetadataItems</a>
</td>
<td align="left" width="63%">
Activate an <b>ISpatialAudioObjectForMetadataItems</b> for rendering. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FD356AA9-F4BC-4864-8A9F-994EB527E123">GetSpatialAudioMetadataItems</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://msdn.microsoft.com/54A6B7DE-A41E-4214-AF02-CC19250B9037">ISpatialAudioMetadataItems</a> object which stores metadata items for  the  <b>ISpatialAudioObjectForMetadataItems</b>.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a> interface.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/54721875-D93A-4C7E-A07E-C286E1A409D3">ISpatialAudioObjectBase</a>
 

 

