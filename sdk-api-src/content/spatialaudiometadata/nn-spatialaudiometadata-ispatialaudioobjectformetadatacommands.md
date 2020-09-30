---
UID: NN:spatialaudiometadata.ISpatialAudioObjectForMetadataCommands
title: ISpatialAudioObjectForMetadataCommands (spatialaudiometadata.h)
description: Used to write metadata commands for spatial audio.
helpviewer_keywords: ["ISpatialAudioObjectForMetadataCommands","ISpatialAudioObjectForMetadataCommands interface [Core Audio]","ISpatialAudioObjectForMetadataCommands interface [Core Audio]","described","coreaudio.ispatialaudioobjectformetadatacommands","spatialaudiometadata/ISpatialAudioObjectForMetadataCommands"]
old-location: coreaudio\ispatialaudioobjectformetadatacommands.htm
tech.root: CoreAudio
ms.assetid: B142D5CC-7321-4F3C-804D-50E728C37D10
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectForMetadataCommands, ISpatialAudioObjectForMetadataCommands interface [Core Audio], ISpatialAudioObjectForMetadataCommands interface [Core Audio],described, coreaudio.ispatialaudioobjectformetadatacommands, spatialaudiometadata/ISpatialAudioObjectForMetadataCommands
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioObjectForMetadataCommands
 - spatialaudiometadata/ISpatialAudioObjectForMetadataCommands
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - spatialaudiometadata.h
api_name:
 - ISpatialAudioObjectForMetadataCommands
---

# ISpatialAudioObjectForMetadataCommands interface


## -description

Used to write metadata commands for spatial audio. Valid commands and value lengths are defined by the metadata format specified in the <a href="/windows/desktop/api/spatialaudiometadata/ns-spatialaudiometadata-spatialaudioobjectrenderstreamformetadataactivationparams">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata">ISpatialAudioObjectRenderStreamForMetadata</a> was created.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioObjectForMetadataCommands</b> interface inherits from <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a>. <b>ISpatialAudioObjectForMetadataCommands</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioObjectForMetadataCommands</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudioobjectformetadatacommands-writenextmetadatacommand">WriteNextMetadataCommand</a>
</td>
<td align="left" width="63%">
Writes a metadata command to the spatial audio object, each command may only be added once per object per processing cycle. Valid commands and value lengths are defined by the metadata format specified in the <a href="/windows/desktop/api/spatialaudiometadata/ns-spatialaudiometadata-spatialaudioobjectrenderstreamformetadataactivationparams">SpatialAudioObjectRenderStreamForMetadataActivationParams</a> when the <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata">ISpatialAudioObjectRenderStreamForMetadata</a> was created.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectbase">ISpatialAudioObjectBase</a> interface.</div>
<div> </div>

## -see-also

<a href="https://msdn.microsoft.com/en-us/library/Mt829727(v=VS.85).aspx">ISpatialAudioObjectBase</a>