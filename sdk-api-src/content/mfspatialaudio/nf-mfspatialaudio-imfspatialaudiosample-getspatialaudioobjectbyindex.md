---
UID: NF:mfspatialaudio.IMFSpatialAudioSample.GetSpatialAudioObjectByIndex
title: IMFSpatialAudioSample::GetSpatialAudioObjectByIndex (mfspatialaudio.h)
description: Returns the spatial audio object, represented by an IMFSpatialAudioObjectBuffer object, corresponding to the specified index.
helpviewer_keywords: ["GetSpatialAudioObjectByIndex","GetSpatialAudioObjectByIndex method [Media Foundation]","GetSpatialAudioObjectByIndex method [Media Foundation]","IMFSpatialAudioSample interface","IMFSpatialAudioSample interface [Media Foundation]","GetSpatialAudioObjectByIndex method","IMFSpatialAudioSample.GetSpatialAudioObjectByIndex","IMFSpatialAudioSample::GetSpatialAudioObjectByIndex","mf.imfspatialaudiosample_getspatialaudioobjectbyindex","mfspatialaudio/IMFSpatialAudioSample::GetSpatialAudioObjectByIndex"]
old-location: mf\imfspatialaudiosample_getspatialaudioobjectbyindex.htm
tech.root: medfound
ms.assetid: 2B5A2D44-BA41-49FC-B4FD-9BCD9EE2D549
ms.date: 12/05/2018
ms.keywords: GetSpatialAudioObjectByIndex, GetSpatialAudioObjectByIndex method [Media Foundation], GetSpatialAudioObjectByIndex method [Media Foundation],IMFSpatialAudioSample interface, IMFSpatialAudioSample interface [Media Foundation],GetSpatialAudioObjectByIndex method, IMFSpatialAudioSample.GetSpatialAudioObjectByIndex, IMFSpatialAudioSample::GetSpatialAudioObjectByIndex, mf.imfspatialaudiosample_getspatialaudioobjectbyindex, mfspatialaudio/IMFSpatialAudioSample::GetSpatialAudioObjectByIndex
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
 - IMFSpatialAudioSample::GetSpatialAudioObjectByIndex
 - mfspatialaudio/IMFSpatialAudioSample::GetSpatialAudioObjectByIndex
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
 - IMFSpatialAudioSample.GetSpatialAudioObjectByIndex
---

# IMFSpatialAudioSample::GetSpatialAudioObjectByIndex


## -description

Returns the spatial audio object, represented by an <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a> object, corresponding to the specified index.

## -parameters

### -param dwIndex

A 32 bit variable with the 0-based index of the requested audio object.

### -param ppAudioObjBuffer

A pointer to an <a href="/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudioobjectbuffer">IMFSpatialAudioObjectBuffer</a> object in which the spatial audio object corresponding with the specified index will be stored.

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