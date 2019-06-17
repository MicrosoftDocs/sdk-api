---
UID: NN:spatialaudiometadata.ISpatialAudioObjectRenderStreamForMetadata
title: ISpatialAudioObjectRenderStreamForMetadata (spatialaudiometadata.h)
author: windows-sdk-content
description: Provides methods for controlling a spatial audio object render stream for metadata, including starting, stopping, and resetting the stream.
old-location: coreaudio\ispatialaudioobjectrenderstreamformetadata.htm
tech.root: CoreAudio
ms.assetid: 1623B280-FC12-4C19-9D4A-D8463D1A1046
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISpatialAudioObjectRenderStreamForMetadata, ISpatialAudioObjectRenderStreamForMetadata interface [Core Audio], ISpatialAudioObjectRenderStreamForMetadata interface [Core Audio],described, coreaudio.ispatialaudioobjectrenderstreamformetadata, spatialaudiometadata/ISpatialAudioObjectRenderStreamForMetadata
ms.topic: interface
f1_keywords: ["spatialaudiometadata/ISpatialAudioObjectRenderStreamForMetadata"]
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
 - ISpatialAudioObjectRenderStreamForMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpatialAudioObjectRenderStreamForMetadata interface


## -description


Provides methods for controlling a spatial audio object render stream for metadata, including starting, stopping, and resetting the stream. Also provides methods for activating new <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectformetadatacommands">ISpatialAudioObjectForMetadataCommands</a> and <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectformetadataitems">ISpatialAudioObjectForMetadataItems</a> instances and notifying the system when you are beginning and ending the process of updating activated spatial audio objects and data.

This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -remarks



<div class="alert"><b>Note</b>  Many of the methods provided by this interface are implemented in the inherited <a href="https://msdn.microsoft.com/en-us/library/Mt829728(v=VS.85).aspx">ISpatialAudioObjectRenderStreamBase</a> interface.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt829728(v=VS.85).aspx">ISpatialAudioObjectRenderStreamBase</a>
 

 

