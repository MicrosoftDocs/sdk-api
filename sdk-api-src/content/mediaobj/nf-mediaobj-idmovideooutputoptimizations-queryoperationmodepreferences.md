---
UID: NF:mediaobj.IDMOVideoOutputOptimizations.QueryOperationModePreferences
title: IDMOVideoOutputOptimizations::QueryOperationModePreferences (mediaobj.h)
description: The QueryOperationModePreferences method retrieves the DMO's preferred optimization features.
helpviewer_keywords: ["IDMOVideoOutputOptimizations interface [DirectShow]","QueryOperationModePreferences method","IDMOVideoOutputOptimizations.QueryOperationModePreferences","IDMOVideoOutputOptimizations::QueryOperationModePreferences","IDMOVideoOutputOptimizationsQueryOperationModePreferences","QueryOperationModePreferences","QueryOperationModePreferences method [DirectShow]","QueryOperationModePreferences method [DirectShow]","IDMOVideoOutputOptimizations interface","dshow.idmovideooutputoptimizations_queryoperationmodepreferences","mediaobj/IDMOVideoOutputOptimizations::QueryOperationModePreferences"]
old-location: dshow\idmovideooutputoptimizations_queryoperationmodepreferences.htm
tech.root: dshow
ms.assetid: 55916330-8395-4952-a349-f1ab5a3a2d64
ms.date: 4/26/2023
ms.keywords: IDMOVideoOutputOptimizations interface [DirectShow],QueryOperationModePreferences method, IDMOVideoOutputOptimizations.QueryOperationModePreferences, IDMOVideoOutputOptimizations::QueryOperationModePreferences, IDMOVideoOutputOptimizationsQueryOperationModePreferences, QueryOperationModePreferences, QueryOperationModePreferences method [DirectShow], QueryOperationModePreferences method [DirectShow],IDMOVideoOutputOptimizations interface, dshow.idmovideooutputoptimizations_queryoperationmodepreferences, mediaobj/IDMOVideoOutputOptimizations::QueryOperationModePreferences
req.header: mediaobj.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMOVideoOutputOptimizations::QueryOperationModePreferences
 - mediaobj/IDMOVideoOutputOptimizations::QueryOperationModePreferences
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IDMOVideoOutputOptimizations.QueryOperationModePreferences
---

# IDMOVideoOutputOptimizations::QueryOperationModePreferences


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>QueryOperationModePreferences</code> method retrieves the DMO's preferred optimization features.

## -parameters

### -param ulOutputStreamIndex

Zero-based index of an output stream on the DMO.

### -param pdwRequestedCapabilities

Pointer to a variable that receives the DMO's requested features. The returned value is a bitwise combination of zero or more flags from the <a href="/windows/desktop/api/mediaobj/ne-mediaobj-_dmo_video_output_stream_flags">DMO_VIDEO_OUTPUT_STREAM_FLAGS</a> enumeration.

## -returns

Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

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

## -see-also

<a href="/windows/desktop/api/mediaobj/nn-mediaobj-idmovideooutputoptimizations">IDMOVideoOutputOptimizations Interface</a>