---
UID: NF:vidcap.ICameraControl.get_PrivacyMode
title: ICameraControl::get_PrivacyMode (vidcap.h)
description: .
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_PrivacyMode method","ICameraControl.get_PrivacyMode","ICameraControl::get_PrivacyMode","ICameraControlget_PrivacyMode","dshow.icameracontrol_get_privacymode","get_PrivacyMode","get_PrivacyMode method [DirectShow]","get_PrivacyMode method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_PrivacyMode"]
old-location: dshow\icameracontrol_get_privacymode.htm
tech.root: dshow
ms.assetid: 22bec1da-65ca-4101-8f30-8fbb537e5678
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],get_PrivacyMode method, ICameraControl.get_PrivacyMode, ICameraControl::get_PrivacyMode, ICameraControlget_PrivacyMode, dshow.icameracontrol_get_privacymode, get_PrivacyMode, get_PrivacyMode method [DirectShow], get_PrivacyMode method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_PrivacyMode
req.header: vidcap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ICameraControl::get_PrivacyMode
 - vidcap/ICameraControl::get_PrivacyMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - ICameraControl.get_PrivacyMode
---

# ICameraControl::get_PrivacyMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_PrivacyMode</code> method returns the camera's privacy setting. The privacy setting controls whether camera sensor captures video.

## -parameters

### -param pValue [out]

Receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>The sensor is able to capture video.</td>
</tr>
<tr>
<td>1</td>
<td>The sensor is not able to capture video.</td>
</tr>
</table>

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>