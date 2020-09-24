---
UID: NN:mfspatialaudio.IMFSpatialAudioSample
title: IMFSpatialAudioSample (mfspatialaudio.h)
description: Represents a multimedia sample with spatial sound information. Every IMFSpatialAudioSample contains one or more IMFSpatialAudioObjectBuffer objects.
helpviewer_keywords: ["IMFSpatialAudioSample","IMFSpatialAudioSample interface [Media Foundation]","IMFSpatialAudioSample interface [Media Foundation]","described","mf.imfspatialaudiosample","mfspatialaudio/IMFSpatialAudioSample"]
old-location: mf\imfspatialaudiosample.htm
tech.root: mf
ms.assetid: EA0277BF-C9C8-42FE-9206-A87FC3C50A9F
ms.date: 12/05/2018
ms.keywords: IMFSpatialAudioSample, IMFSpatialAudioSample interface [Media Foundation], IMFSpatialAudioSample interface [Media Foundation],described, mf.imfspatialaudiosample, mfspatialaudio/IMFSpatialAudioSample
req.header: mfspatialaudio.h
req.include-header: Mfobjects.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfobjects.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSpatialAudioSample
 - mfspatialaudio/IMFSpatialAudioSample
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfobjects.lib
 - mfobjects.dll
api_name:
 - IMFSpatialAudioSample
---

# IMFSpatialAudioSample interface


## -description

Represents a multimedia sample with spatial sound information. Every <b>IMFSpatialAudioSample</b> contains one or more <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a> objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFSpatialAudioSample</b> interface inherits from <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>. <b>IMFSpatialAudioSample</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFSpatialAudioSample</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudiosample-addspatialaudioobject">AddSpatialAudioObject</a>
</td>
<td align="left" width="63%">
Adds a new spatial audio object, represented by an <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a> object, to the     sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudiosample-getobjectcount">GetObjectCount</a>
</td>
<td align="left" width="63%">
Gets the count of spatial audio objects, represented by <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a> objects, in the sample.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/mfspatialaudio/nf-mfspatialaudio-imfspatialaudiosample-getspatialaudioobjectbyindex">GetSpatialAudioObjectByIndex</a>
</td>
<td align="left" width="63%">
Returns the spatial audio object, represented by an <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a> object, corresponding to the specified index.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>