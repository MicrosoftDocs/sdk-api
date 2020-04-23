---
UID: NN:spatialaudiometadata.ISpatialAudioMetadataClient
title: ISpatialAudioMetadataClient (spatialaudiometadata.h)
description: Provides a class factory for creating ISpatialAudioMetadataItems, ISpatialAudioMetadataWriter, ISpatialAudioMetadataReader, and ISpatialAudioMetadataCopier objects.helpviewer_keywords: ["ISpatialAudioMetadataClient","ISpatialAudioMetadataClient interface [Core Audio]","ISpatialAudioMetadataClient interface [Core Audio]","described","coreaudio.ispatialaudiometadataclient","spatialaudiometadata/ISpatialAudioMetadataClient"]
old-location: coreaudio\ispatialaudiometadataclient.htm
tech.root: CoreAudio
ms.assetid: 42EDD4D2-3DAA-4F8F-A71C-7EDFEBBCB3FB
ms.date: 12/05/2018
ms.keywords: ISpatialAudioMetadataClient, ISpatialAudioMetadataClient interface [Core Audio], ISpatialAudioMetadataClient interface [Core Audio],described, coreaudio.ispatialaudiometadataclient, spatialaudiometadata/ISpatialAudioMetadataClient
f1_keywords:
- spatialaudiometadata/ISpatialAudioMetadataClient
dev_langs:
- c++
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
- ISpatialAudioMetadataClient
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISpatialAudioMetadataClient interface


## -description



Provides a class factory for creating
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a>, <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a>, <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader">ISpatialAudioMetadataReader</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatacopier">ISpatialAudioMetadataCopier</a> objects.
When an <b>ISpatialAudioMetadataItems</b> is activated, a metadata format  ID is specified,     which defines the metadata format enforced for all objects created from this factory.
If the specified format is not supported by the current audio render endpoint, the class factory will not successfully activate the interface and will return an error.



This interface is a part of  Windows Sonic, Microsoft’s audio platform for more immersive audio which includes integrated spatial sound on Xbox and Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISpatialAudioMetadataClient</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISpatialAudioMetadataClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISpatialAudioMetadataClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadatacopier">ActivateSpatialAudioMetadataCopier</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> object for copying spatial audio metadata items from one <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object to another.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadataitems">ActivateSpatialAudioMetadataItems</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object for storing spatial audio metadata items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadatareader">ActivateSpatialAudioMetadataReader</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> object for reading spatial audio metadata items from an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-activatespatialaudiometadatawriter">ActivateSpatialAudioMetadataWriter</a>
</td>
<td align="left" width="63%">
Creates an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter">ISpatialAudioMetadataWriter</a> object for writing spatial audio metadata items to an <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitems">ISpatialAudioMetadataItems</a> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nf-spatialaudiometadata-ispatialaudiometadataclient-getspatialaudiometadataitemsbufferlength">GetSpatialAudioMetadataItemsBufferLength</a>
</td>
<td align="left" width="63%">
Gets the length of the buffer required to store the specified number of spatial audio metadata items. Use this method to determine the correct buffer size to use when attaching caller-provided memory through the <a href="https://docs.microsoft.com/windows/desktop/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadataitemsbuffer">ISpatialAudioMetadataItemsBuffer</a> interface.

</td>
</tr>
</table> 

