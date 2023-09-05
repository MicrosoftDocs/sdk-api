---
UID: NF:vidcap.ICameraControl.put_PrivacyMode
title: ICameraControl::put_PrivacyMode (vidcap.h)
description: The put_PrivacyMode method sets the camera's privacy setting. The privacy setting controls whether the camera sensor captures video.
helpviewer_keywords: ["ICameraControl interface [DirectShow]","put_PrivacyMode method","ICameraControl.put_PrivacyMode","ICameraControl::put_PrivacyMode","ICameraControlput_PrivacyMode","dshow.icameracontrol_put_privacymode","put_PrivacyMode","put_PrivacyMode method [DirectShow]","put_PrivacyMode method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::put_PrivacyMode"]
old-location: dshow\icameracontrol_put_privacymode.htm
tech.root: dshow
ms.assetid: 04116eba-926c-43fc-9a45-91be42e9af26
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],put_PrivacyMode method, ICameraControl.put_PrivacyMode, ICameraControl::put_PrivacyMode, ICameraControlput_PrivacyMode, dshow.icameracontrol_put_privacymode, put_PrivacyMode, put_PrivacyMode method [DirectShow], put_PrivacyMode method [DirectShow],ICameraControl interface, vidcap/ICameraControl::put_PrivacyMode
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
 - ICameraControl::put_PrivacyMode
 - vidcap/ICameraControl::put_PrivacyMode
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
 - ICameraControl.put_PrivacyMode
---

# ICameraControl::put_PrivacyMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_PrivacyMode</code> method sets the camera's privacy setting. The privacy setting controls whether the camera sensor captures video.

## -parameters

### -param Value [in]

Specifies one of the following values.

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

### -param Flags [in]

Zero or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>. If the CameraControl_Flags_Auto flag is used, the <i>Value</i> parameter is ignored and the camera sets the default value.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>