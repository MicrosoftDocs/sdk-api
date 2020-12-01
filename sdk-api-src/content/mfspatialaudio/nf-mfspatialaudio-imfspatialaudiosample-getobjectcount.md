---
UID: NF:mfspatialaudio.IMFSpatialAudioSample.GetObjectCount
title: IMFSpatialAudioSample::GetObjectCount (mfspatialaudio.h)
description: Gets the count of spatial audio objects, represented by IMFSpatialAudioObjectBuffer objects, in the sample.
helpviewer_keywords: ["GetObjectCount","GetObjectCount method [Media Foundation]","GetObjectCount method [Media Foundation]","IMFSpatialAudioSample interface","IMFSpatialAudioSample interface [Media Foundation]","GetObjectCount method","IMFSpatialAudioSample.GetObjectCount","IMFSpatialAudioSample::GetObjectCount","mf.imfspatialaudiosample_getobjectcount","mfspatialaudio/IMFSpatialAudioSample::GetObjectCount"]
old-location: mf\imfspatialaudiosample_getobjectcount.htm
tech.root: mf
ms.assetid: D386E482-4C5A-4F8A-801F-EA1AD4C9157C
ms.date: 12/05/2018
ms.keywords: GetObjectCount, GetObjectCount method [Media Foundation], GetObjectCount method [Media Foundation],IMFSpatialAudioSample interface, IMFSpatialAudioSample interface [Media Foundation],GetObjectCount method, IMFSpatialAudioSample.GetObjectCount, IMFSpatialAudioSample::GetObjectCount, mf.imfspatialaudiosample_getobjectcount, mfspatialaudio/IMFSpatialAudioSample::GetObjectCount
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
 - IMFSpatialAudioSample::GetObjectCount
 - mfspatialaudio/IMFSpatialAudioSample::GetObjectCount
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
 - IMFSpatialAudioSample.GetObjectCount
---

# IMFSpatialAudioSample::GetObjectCount


## -description

Gets the count of spatial audio objects, represented by <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a> objects, in the sample.

## -parameters

### -param pdwObjectCount [out]

A pointer to a 32 bit variable where the total number of audio objects in the sample will be stored.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
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

## -see-also

<a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample">IMFSpatialAudioSample</a>