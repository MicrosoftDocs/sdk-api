---
UID: NF:vidcap.ICameraControl.get_ScanMode
title: ICameraControl::get_ScanMode (vidcap.h)
description: The get_ScanMode method returns the current scanning mode (interlaced or progressive).
helpviewer_keywords: ["ICameraControl interface [DirectShow]","get_ScanMode method","ICameraControl.get_ScanMode","ICameraControl::get_ScanMode","ICameraControlget_ScanMode","dshow.icameracontrol_get_scanmode","get_ScanMode","get_ScanMode method [DirectShow]","get_ScanMode method [DirectShow]","ICameraControl interface","vidcap/ICameraControl::get_ScanMode"]
old-location: dshow\icameracontrol_get_scanmode.htm
tech.root: dshow
ms.assetid: 09a75986-9c5d-44fc-af62-297481854574
ms.date: 4/26/2023
ms.keywords: ICameraControl interface [DirectShow],get_ScanMode method, ICameraControl.get_ScanMode, ICameraControl::get_ScanMode, ICameraControlget_ScanMode, dshow.icameracontrol_get_scanmode, get_ScanMode, get_ScanMode method [DirectShow], get_ScanMode method [DirectShow],ICameraControl interface, vidcap/ICameraControl::get_ScanMode
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
 - ICameraControl::get_ScanMode
 - vidcap/ICameraControl::get_ScanMode
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
 - ICameraControl.get_ScanMode
---

# ICameraControl::get_ScanMode


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_ScanMode</code> method returns the current scanning mode (interlaced or progressive).

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
<td>Interlaced video.</td>
</tr>
<tr>
<td>1</td>
<td>Progressive video.</td>
</tr>
</table>

### -param pFlags [out]

Receives one or more flags. See <a href="/windows/win32/api/strmif/ne-strmif-cameracontrolflags">CameraControlFlags</a>.

## -returns

Returns an <b>HRESULT</b> value.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vidcap/nn-vidcap-icameracontrol">ICameraControl Interface</a>