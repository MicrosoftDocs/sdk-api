---
UID: NF:qnetwork.IAMExtendedSeeking.GetMarkerName
title: IAMExtendedSeeking::GetMarkerName (qnetwork.h)
description: The GetMarkerName method retrieves the name associated with the specified marker.
helpviewer_keywords: ["GetMarkerName","GetMarkerName method [DirectShow]","GetMarkerName method [DirectShow]","IAMExtendedSeeking interface","IAMExtendedSeeking interface [DirectShow]","GetMarkerName method","IAMExtendedSeeking.GetMarkerName","IAMExtendedSeeking::GetMarkerName","IAMExtendedSeekingGetMarkerName","dshow.iamextendedseeking_getmarkername","qnetwork/IAMExtendedSeeking::GetMarkerName"]
old-location: dshow\iamextendedseeking_getmarkername.htm
tech.root: dshow
ms.assetid: 899cc32e-3a9f-4be0-97a9-2ddd323bf9ce
ms.date: 4/26/2023
ms.keywords: GetMarkerName, GetMarkerName method [DirectShow], GetMarkerName method [DirectShow],IAMExtendedSeeking interface, IAMExtendedSeeking interface [DirectShow],GetMarkerName method, IAMExtendedSeeking.GetMarkerName, IAMExtendedSeeking::GetMarkerName, IAMExtendedSeekingGetMarkerName, dshow.iamextendedseeking_getmarkername, qnetwork/IAMExtendedSeeking::GetMarkerName
req.header: qnetwork.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMExtendedSeeking::GetMarkerName
 - qnetwork/IAMExtendedSeeking::GetMarkerName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMExtendedSeeking.GetMarkerName
---

# IAMExtendedSeeking::GetMarkerName


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetMarkerName</code> method retrieves the name associated with the specified marker.

## -parameters

### -param MarkerNum [in]

Specifies the marker number.

### -param pbstrMarkerName [out]

Pointer to a variable that receives the marker name.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/windows/desktop/api/qnetwork/nn-qnetwork-iamextendedseeking">IAMExtendedSeeking Interface</a>



<a href="/windows/desktop/api/qnetwork/nf-qnetwork-iamextendedseeking-getmarkertime">IAMExtendedSeeking::GetMarkerTime</a>