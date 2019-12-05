---
UID: NN:spatialaudiometadata.ISpatialAudioObjectForMetadataItems
title: ISpatialAudioObjectForMetadataItems (spatialaudiometadata.h)
description: Used to write spatial audio metadata for applications that require multiple metadata items per buffer with frame-accurate placement.
old-location: coreaudio\ispatialaudioobjectformetadataitems.htm
tech.root: CoreAudio
ms.assetid: 4861D2AA-E685-4A72-BE98-6FEEB72ACF67
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectForMetadataItems, ISpatialAudioObjectForMetadataItems interface [Core Audio], ISpatialAudioObjectForMetadataItems interface [Core Audio],described, coreaudio.ispatialaudioobjectformetadataitems, spatialaudiometadata/ISpatialAudioObjectForMetadataItems
ms.topic: interface
f1_keywords:
- spatialaudiometadata/ISpatialAudioObjectForMetadataItems
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpatialAudioObjectForMetadataItems interface


## -description


 Used to write spatial audio metadata for applications that require multiple metadata items per buffer with frame-accurate placement.  The data written via this interface must adhere to the format defined by the metadata format specified in the <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/ns-spatialaudiometadata-spatialaudioobjectrenderstreamformetadataactivationparams">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata">ISpatialAudioObjectRenderStreamForMetadata</a> was created.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectForMetadataItems</b> interface inherits from <a href="https://docs.microsoft.com/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>. <b>ISpatialAudioObjectForMetadataItems</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata-activatespatialaudioobjectformetadatacommands">ActivateSpatialAudioObjectForMetadataCommands</a>
</td>
<td align="left" width="63%">
Activate an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectformetadatacommands">ISpatialAudioObjectForMetadataCommands</a> for rendering. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata-activatespatialaudioobjectformetadataitems">ActivateSpatialAudioObjectForMetadataItems</a>
</td>
<td align="left" width="63%">
Activate an <b>ISpatialAudioObjectForMetadataItems</b> for rendering. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudioobjectformetadataitems-getspatialaudiometadataitems">GetSpatialAudioMetadataItems</a>
</td>
<td align="left" width="63%">
Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object which stores metadata items for  the  <b>ISpatialAudioObjectForMetadataItems</b>.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="https://docs.microsoft.com/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a> interface.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/en-us/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>
 

 

