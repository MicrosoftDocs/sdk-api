---
UID: NF:amvideo.IDirectDrawVideo.GetFourCCCodes
title: IDirectDrawVideo::GetFourCCCodes (amvideo.h)
description: The GetFourCCCodes method retrieves the multimedia format type.
helpviewer_keywords: ["GetFourCCCodes","GetFourCCCodes method [DirectShow]","GetFourCCCodes method [DirectShow]","IDirectDrawVideo interface","IDirectDrawVideo interface [DirectShow]","GetFourCCCodes method","IDirectDrawVideo.GetFourCCCodes","IDirectDrawVideo::GetFourCCCodes","IDirectDrawVideoGetFourCCCodes","amvideo/IDirectDrawVideo::GetFourCCCodes","dshow.idirectdrawvideo_getfourcccodes"]
old-location: dshow\idirectdrawvideo_getfourcccodes.htm
tech.root: dshow
ms.assetid: 3ea1c5c4-bf2e-40f6-bf48-a69900128ec8
ms.date: 4/26/2023
ms.keywords: GetFourCCCodes, GetFourCCCodes method [DirectShow], GetFourCCCodes method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],GetFourCCCodes method, IDirectDrawVideo.GetFourCCCodes, IDirectDrawVideo::GetFourCCCodes, IDirectDrawVideoGetFourCCCodes, amvideo/IDirectDrawVideo::GetFourCCCodes, dshow.idirectdrawvideo_getfourcccodes
req.header: amvideo.h
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
 - IDirectDrawVideo::GetFourCCCodes
 - amvideo/IDirectDrawVideo::GetFourCCCodes
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
 - IDirectDrawVideo.GetFourCCCodes
---

# IDirectDrawVideo::GetFourCCCodes


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetFourCCCodes</code> method retrieves the multimedia format type.

## -parameters

### -param pCount

Pointer to the number of FOURCC codes in the <i>pCodes</i> array.

### -param pCodes

Pointer to an array of <b>DWORD</b> media tags formerly used for Microsoft multimedia types.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as <i>FOURCC</i> codes. Because FOURCC codes are unique, a one-to-one mapping has been made possible by allocating a range of 4 billion GUIDs representing FOURCCs.

This method retrieves the FOURCC codes that the current display driver can support. The number available is obtained by calling the method with a valid <i>pCount</i> pointer, but with <i>pCodes</i> set to <b>NULL</b>. In this case, the <i>pCount</i> variable will be filled in with the number of FOURCC codes available. An application can then allocate enough <b>DWORD</b> values for this many FOURCC codes and call the method again with the array pointer in <i>pCodes</i>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>