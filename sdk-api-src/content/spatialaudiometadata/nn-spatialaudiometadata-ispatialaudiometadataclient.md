---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataClient
title: ISpatialAudioMetadataClient (spatialaudiometadata.h)
description: Provides a class factory for creating ISpatialAudioMetadataItems, ISpatialAudioMetadataWriter, ISpatialAudioMetadataReader, and ISpatialAudioMetadataCopier objects.
helpviewer_keywords: ["ISpatialAudioMetadataClient","ISpatialAudioMetadataClient interface [Core Audio]","ISpatialAudioMetadataClient interface [Core Audio]","described","coreaudio.ispatialaudiometadataclient","spatialaudiometadata/ISpatialAudioMetadataClient"]
old-location: coreaudio\ispatialaudiometadataclient.htm
tech.root: CoreAudio
ms.assetid: 42EDD4D2-3DAA-4F8F-A71C-7EDFEBBCB3FB
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataClient, ISpatialAudioMetadataClient interface [Core Audio], ISpatialAudioMetadataClient interface [Core Audio],described, coreaudio.ispatialaudiometadataclient, spatialaudiometadata/ISpatialAudioMetadataClient
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISpatialAudioMetadataClient
 - spatialaudiometadata/ISpatialAudioMetadataClient
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SpatialAudioMetadata.h
api_name:
 - ISpatialAudioMetadataClient
---

# ISpatialAudioMetadataClient interface


## -description

Provides a class factory for creating
<a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a>, <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a>, <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>, and <a href="/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatacopier">ISpatialAudioMetadataCopier</a> objects.
When an <b>ISpatialAudioMetadataItems</b> is activated, a metadata format  ID is specified,     which defines the metadata format enforced for all objects created from this factory.
If the specified format is not supported by the current audio render endpoint, the class factory will not successfully activate the interface and will return an error.



This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.

## -inheritance

The <b>ISpatialAudioMetadataClient</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioMetadataClient</b> also has these types of members:

