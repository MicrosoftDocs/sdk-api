---
UID: NN:mfreadwrite.IMFSinkWriterEncoderConfig
title: IMFSinkWriterEncoderConfig (mfreadwrite.h)
description: Provides additional functionality on the sink writer for dynamically changing the media type and encoder configuration.helpviewer_keywords: ["IMFSinkWriterEncoderConfig","IMFSinkWriterEncoderConfig interface [Media Foundation]","IMFSinkWriterEncoderConfig interface [Media Foundation]","described","mf.imfsinkwriterencoderconfig","mfreadwrite/IMFSinkWriterEncoderConfig"]
old-location: mf\imfsinkwriterencoderconfig.htm
tech.root: medfound
ms.assetid: 3a0d090d-9eb1-4624-989b-c5da27b988aa
ms.date: 12/05/2018
ms.keywords: IMFSinkWriterEncoderConfig, IMFSinkWriterEncoderConfig interface [Media Foundation], IMFSinkWriterEncoderConfig interface [Media Foundation],described, mf.imfsinkwriterencoderconfig, mfreadwrite/IMFSinkWriterEncoderConfig
f1_keywords:
- mfreadwrite/IMFSinkWriterEncoderConfig
dev_langs:
- c++
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfreadwrite.idl
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
- mfreadwrite.h
api_name:
- IMFSinkWriterEncoderConfig
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFSinkWriterEncoderConfig interface


## -description


Provides additional functionality on the sink writer for dynamically changing the media type and encoder configuration. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSinkWriterEncoderConfig</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFSinkWriterEncoderConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSinkWriterEncoderConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriterencoderconfig-placeencodingparameters">PlaceEncodingParameters</a>
</td>
<td align="left" width="63%">
Dynamically updates the encoder configuration with a collection of new encoder settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriterencoderconfig-settargetmediatype">SetTargetMediaType</a>
</td>
<td align="left" width="63%">
Dynamically changes the target media type that Sink Writer is encoding to. 

</td>
</tr>
</table> 


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/medfound/sink-writer">Sink Writer</a> implements this interface in Windows 8.1. To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the <a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter">IMFSinkWriter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriterex">IMFSinkWriterEx</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

