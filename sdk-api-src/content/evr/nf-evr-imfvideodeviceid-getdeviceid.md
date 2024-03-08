---
UID: NF:evr.IMFVideoDeviceID.GetDeviceID
title: IMFVideoDeviceID::GetDeviceID (evr.h)
description: Returns the identifier of the video device supported by an EVR mixer or presenter.
helpviewer_keywords: ["GetDeviceID","GetDeviceID method [Media Foundation]","GetDeviceID method [Media Foundation]","IMFVideoDeviceID interface","IMFVideoDeviceID interface [Media Foundation]","GetDeviceID method","IMFVideoDeviceID.GetDeviceID","IMFVideoDeviceID::GetDeviceID","e23ebce0-be58-413a-ab71-d94811c96029","evr/IMFVideoDeviceID::GetDeviceID","mf.imfvideodeviceid_getdeviceid"]
old-location: mf\imfvideodeviceid_getdeviceid.htm
tech.root: mfarchive
ms.assetid: e23ebce0-be58-413a-ab71-d94811c96029
ms.date: 12/05/2018
ms.keywords: GetDeviceID, GetDeviceID method [Media Foundation], GetDeviceID method [Media Foundation],IMFVideoDeviceID interface, IMFVideoDeviceID interface [Media Foundation],GetDeviceID method, IMFVideoDeviceID.GetDeviceID, IMFVideoDeviceID::GetDeviceID, e23ebce0-be58-413a-ab71-d94811c96029, evr/IMFVideoDeviceID::GetDeviceID, mf.imfvideodeviceid_getdeviceid
req.header: evr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoDeviceID::GetDeviceID
 - evr/IMFVideoDeviceID::GetDeviceID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDeviceID.GetDeviceID
archived: true
---

# IMFVideoDeviceID::GetDeviceID


## -description

[The component described on this page, [Enhanced Video Renderer](/windows/win32/medfound/enhanced-video-renderer), is a legacy feature. It has been superseded by the Simple Video Renderer (SVR) exposed through the [MediaPlayer](/uwp/api/windows.media.playback.mediaplayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine) components. To play video content you should send data into one of these components and allow them to instantiate the new video renderer.  These components have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** or the lower level **IMFMediaEngine** APIs to play video media in Windows instead of the EVR, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.]

Returns the identifier of the video device supported by an EVR mixer or presenter.

## -parameters

### -param pDeviceID [out]

Receives the device identifier. Generally, the value is IID_IDirect3DDevice9.

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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The video renderer has been shut down.

</td>
</tr>
</table>

## -remarks

If a mixer or presenter uses Direct3D 9, it must return the value IID_IDirect3DDevice9 in <i>pDeviceID</i>. The EVR's default mixer and presenter both return this value. If you write a custom mixer or presenter, it can return some other value. However, the mixer and presenter must use matching device identifiers.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr/nn-evr-imfvideodeviceid">IMFVideoDeviceID</a>