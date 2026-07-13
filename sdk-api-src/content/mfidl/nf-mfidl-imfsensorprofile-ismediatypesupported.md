---
UID: NF:mfidl.IMFSensorProfile.IsMediaTypeSupported
title: IMFSensorProfile::IsMediaTypeSupported (mfidl.h)
description: Determines if a media stream supports the specified media type.
helpviewer_keywords: ["IMFSensorProfile interface [Media Foundation]","IsMediaTypeSupported method","IMFSensorProfile.IsMediaTypeSupported","IMFSensorProfile::IsMediaTypeSupported","IsMediaTypeSupported","IsMediaTypeSupported method [Media Foundation]","IsMediaTypeSupported method [Media Foundation]","IMFSensorProfile interface","mf.imfsensorprofile_ismediatypesupported","mfidl/IMFSensorProfile::IsMediaTypeSupported"]
old-location: mf\imfsensorprofile_ismediatypesupported.htm
tech.root: mf
ms.assetid: 9535AF14-A6DF-49E9-B264-734B96A3DC29
ms.date: 12/05/2018
ms.keywords: IMFSensorProfile interface [Media Foundation],IsMediaTypeSupported method, IMFSensorProfile.IsMediaTypeSupported, IMFSensorProfile::IsMediaTypeSupported, IsMediaTypeSupported, IsMediaTypeSupported method [Media Foundation], IsMediaTypeSupported method [Media Foundation],IMFSensorProfile interface, mf.imfsensorprofile_ismediatypesupported, mfidl/IMFSensorProfile::IsMediaTypeSupported
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfsensorgroup.lib
req.dll: Mfsensorgroup.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSensorProfile::IsMediaTypeSupported
 - mfidl/IMFSensorProfile::IsMediaTypeSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mfsensorgroup.dll
api_name:
 - IMFSensorProfile.IsMediaTypeSupported
---

# IMFSensorProfile::IsMediaTypeSupported


## -description

Determines if a media stream supports the specified media type.

## -parameters

### -param StreamId [in]

The ID of the stream to check.

### -param pMediaType [in]

Pointer to an <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> describing the media type to check.

### -param pfSupported [out]

Returns <b>true</b> if the media type is supported; otherwise, <b>false</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfsensorprofile">IMFSensorProfile</a>