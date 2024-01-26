---
UID: NF:evr.IEVRFilterConfigEx.SetConfigPrefs
title: IEVRFilterConfigEx::SetConfigPrefs (evr.h)
description: Sets the configuration parameters for the Microsoft DirectShow Enhanced Video Renderer Filter (EVR).
helpviewer_keywords: ["IEVRFilterConfigEx interface [Media Foundation]","SetConfigPrefs method","IEVRFilterConfigEx.SetConfigPrefs","IEVRFilterConfigEx::SetConfigPrefs","SetConfigPrefs","SetConfigPrefs method [Media Foundation]","SetConfigPrefs method [Media Foundation]","IEVRFilterConfigEx interface","evr/IEVRFilterConfigEx::SetConfigPrefs","mf.ievrfilterconfigex_setconfigprefs"]
old-location: mf\ievrfilterconfigex_setconfigprefs.htm
tech.root: mfarchive
ms.assetid: 6a565c7a-a8d7-433b-b454-262661c2c084
ms.date: 12/05/2018
ms.keywords: IEVRFilterConfigEx interface [Media Foundation],SetConfigPrefs method, IEVRFilterConfigEx.SetConfigPrefs, IEVRFilterConfigEx::SetConfigPrefs, SetConfigPrefs, SetConfigPrefs method [Media Foundation], SetConfigPrefs method [Media Foundation],IEVRFilterConfigEx interface, evr/IEVRFilterConfigEx::SetConfigPrefs, mf.ievrfilterconfigex_setconfigprefs
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IEVRFilterConfigEx::SetConfigPrefs
 - evr/IEVRFilterConfigEx::SetConfigPrefs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - evr.h
api_name:
 - IEVRFilterConfigEx.SetConfigPrefs
archived: true
---

# IEVRFilterConfigEx::SetConfigPrefs


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Sets the configuration parameters for the Microsoft DirectShow <a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer Filter</a> (EVR).

## -parameters

### -param dwConfigFlags [in]

Bitwise <b>OR</b> of  zero or more flags from the <a href="/windows/win32/api/evr/ne-evr-evrfilterconfigprefs">EVRFilterConfigPrefs</a> enumeration.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/enhanced-video-renderer-filter">Enhanced Video Renderer Filter</a>



<a href="/windows/desktop/api/evr/nn-evr-ievrfilterconfigex">IEVRFilterConfigEx</a>



<a href="/windows/desktop/medfound/video-quality-management">Video Quality Management</a>