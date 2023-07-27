---
UID: NF:dmoreg.DMORegister
title: DMORegister function (dmoreg.h)
description: The DMORegister function registers a DMO.
helpviewer_keywords: ["DMORegister","DMORegister function [DirectShow]","dmoreg/DMORegister","dshow.dmoregister"]
old-location: dshow\dmoregister.htm
tech.root: dshow
ms.assetid: 4e70569b-8502-4eee-bd23-173269b345d1
ms.date: 4/26/2023
ms.keywords: DMORegister, DMORegister function [DirectShow], dmoreg/DMORegister, dshow.dmoregister
req.header: dmoreg.h
req.include-header: Dmo.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DMORegister
 - dmoreg/DMORegister
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdmo.dll
api_name:
 - DMORegister
---

# DMORegister function


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DMORegister</b> function registers a DMO.

## -parameters

### -param szName

NULL-terminated string that contains a descriptive name for the DMO. Names longer than 79 characters might be truncated.

### -param clsidDMO

Class identifier (CLSID) of the DMO.

### -param guidCategory

GUID that specifies the category of the DMO. See <a href="/windows/desktop/DirectShow/dmo-guids">DMO GUIDs</a> for a list of category GUIDs.

### -param dwFlags

Bitwise combination of zero or more flags from the <a href="/windows/desktop/api/dmoreg/ne-dmoreg-dmo_register_flags">DMO_REGISTER_FLAGS</a> enumeration.

### -param cInTypes

Number of input media types to register. Can be zero.

### -param pInTypes

Pointer to an array of <a href="/previous-versions/windows/desktop/api/dmoreg/ns-dmoreg-dmo_partial_mediatype">DMO_PARTIAL_MEDIATYPE</a> structures that specify the input media types. The size of the array is specified in the cInTypes parameter

### -param cOutTypes

Number of output media types to register.

### -param pOutTypes

Pointer to an array of DMO_PARTIAL_MEDIATYPE structures that specify the output media types. The size of the array is specified in the cOutTypes parameter. Can be zero.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

This function adds information about a DMO to the registry. Applications or software components can use this information to locate the DMOs they need to use, by calling the <a href="/windows/desktop/api/dmoreg/nf-dmoreg-dmoenum">DMOEnum</a> function. For example, to encode a video stream, you would search in the DMOCATEGORY_VIDEO_ENCODER category for a DMO whose media types matched your requirements.
        

The media types registered by this function are only for the purpose of finding the DMO. They do not necessarily match the types returned by the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getinputtype">IMediaObject::GetInputType</a> and <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype">IMediaObject::GetOutputType</a> methods. For example, a decoder might register just its main input types. After the DMO is created and its input type has been set, its <b>GetOutputType</b> method will return all of the decompressed types it can generate.

## -see-also

<a href="/windows/desktop/DirectShow/dmo-functions">DMO Functions</a>