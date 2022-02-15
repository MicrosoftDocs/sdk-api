---
UID: NF:mfapi.MFWrapMediaType
title: MFWrapMediaType function (mfapi.h)
description: Creates a media type that wraps another media type.
helpviewer_keywords: ["MFWrapMediaType","MFWrapMediaType function [Media Foundation]","a3dd74bc-1f1c-40b9-a43e-d45ff621248f","mf.mfwrapmediatype","mfapi/MFWrapMediaType"]
old-location: mf\mfwrapmediatype.htm
tech.root: mf
ms.assetid: a3dd74bc-1f1c-40b9-a43e-d45ff621248f
ms.date: 12/05/2018
ms.keywords: MFWrapMediaType, MFWrapMediaType function [Media Foundation], a3dd74bc-1f1c-40b9-a43e-d45ff621248f, mf.mfwrapmediatype, mfapi/MFWrapMediaType
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFWrapMediaType
 - mfapi/MFWrapMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFWrapMediaType
---

# MFWrapMediaType function


## -description

Creates a media type that wraps another media type.

## -parameters

### -param pOrig

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the media type to wrap in a new media type.

### -param MajorType

A 
            GUID that specifies the major type for the new media type. For a list of possible values, see <a href="/windows/desktop/medfound/media-type-guids">Major Media Types</a>.

### -param SubType

A 
            GUID that specifies the subtype for the new media type. For possible values, see:

<ul>
<li>
<a href="/windows/desktop/DirectShow/audio-subtypes">Audio Subtypes</a>
</li>
<li>
<a href="/windows/desktop/DirectShow/video-subtypes">Video Subtypes</a>
</li>
</ul>
Applications can define custom subtype GUIDs.

### -param ppWrap

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype">IMFMediaType</a> interface of the new media type that wraps the original media type. The caller must release the interface.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The original media type (<i>pOrig</i>) is stored in the new media type under the <a href="/windows/desktop/medfound/mf-mt-wrapped-type-attribute">MF_MT_WRAPPED_TYPE</a> attribute. To extract the original media type, call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype">MFUnwrapMediaType</a>.
      

This function is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>