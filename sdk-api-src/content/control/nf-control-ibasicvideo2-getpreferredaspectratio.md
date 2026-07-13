---
UID: NF:control.IBasicVideo2.GetPreferredAspectRatio
title: IBasicVideo2::GetPreferredAspectRatio (control.h)
description: The GetPreferredAspectRatio method retrieves the preferred aspect ratio.
helpviewer_keywords: ["GetPreferredAspectRatio","GetPreferredAspectRatio method [DirectShow]","GetPreferredAspectRatio method [DirectShow]","IBasicVideo2 interface","IBasicVideo2 interface [DirectShow]","GetPreferredAspectRatio method","IBasicVideo2.GetPreferredAspectRatio","IBasicVideo2::GetPreferredAspectRatio","IBasicVideo2GetPreferredAspectRatio","control/IBasicVideo2::GetPreferredAspectRatio","dshow.ibasicvideo2_getpreferredaspectratio"]
old-location: dshow\ibasicvideo2_getpreferredaspectratio.htm
tech.root: dshow
ms.assetid: eabfb5a3-201c-483c-81d6-efd19a4b5cef
ms.date: 4/26/2023
ms.keywords: GetPreferredAspectRatio, GetPreferredAspectRatio method [DirectShow], GetPreferredAspectRatio method [DirectShow],IBasicVideo2 interface, IBasicVideo2 interface [DirectShow],GetPreferredAspectRatio method, IBasicVideo2.GetPreferredAspectRatio, IBasicVideo2::GetPreferredAspectRatio, IBasicVideo2GetPreferredAspectRatio, control/IBasicVideo2::GetPreferredAspectRatio, dshow.ibasicvideo2_getpreferredaspectratio
req.header: control.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IBasicVideo2::GetPreferredAspectRatio
 - control/IBasicVideo2::GetPreferredAspectRatio
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
 - IBasicVideo2.GetPreferredAspectRatio
---

# IBasicVideo2::GetPreferredAspectRatio


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetPreferredAspectRatio</code> method retrieves the preferred aspect ratio.

## -parameters

### -param plAspectX [out]

Pointer to a value that indicates the x-axis aspect ratio.

### -param plAspectY [out]

Pointer to a value that indicates the y-axis aspect ratio.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or both of the parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The renderer does not implement <b>IBasicVideo2</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo2">IBasicVideo2 Interface</a>