---
UID: NN:strmif.ICreateDevEnum
title: ICreateDevEnum (strmif.h)
description: The ICreateDevEnum interface creates an enumerator for a category of filters, such as video capture devices or audio capture devices.
helpviewer_keywords: ["ICreateDevEnum","ICreateDevEnum interface [DirectShow]","ICreateDevEnum interface [DirectShow]","described","ICreateDevEnumInterface","dshow.icreatedevenum","strmif/ICreateDevEnum"]
old-location: dshow\icreatedevenum.htm
tech.root: dshow
ms.assetid: fc300bb8-aea4-4848-af43-a70a7fb8c07c
ms.date: 4/26/2023
ms.keywords: ICreateDevEnum, ICreateDevEnum interface [DirectShow], ICreateDevEnum interface [DirectShow],described, ICreateDevEnumInterface, dshow.icreatedevenum, strmif/ICreateDevEnum
req.header: strmif.h
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
 - ICreateDevEnum
 - strmif/ICreateDevEnum
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
 - ICreateDevEnum
---

# ICreateDevEnum interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>ICreateDevEnum</b> interface creates an enumerator for a category of filters, such as video capture devices or audio capture devices. The <a href="/windows/desktop/DirectShow/system-device-enumerator">System Device Enumerator</a> exposes this interface.

Applications can use this interface to enumerate filters within a category. The <a href="/windows/desktop/api/strmif/nf-strmif-icreatedevenum-createclassenumerator">CreateClassEnumerator</a> method returns an enumerator object for a specific filter category. The enumerator object supports the <a href="/windows/desktop/api/objidl/nn-objidl-ienummoniker">IEnumMoniker</a> interface and returns a list of monikers, where each moniker represents a filter.

In some cases, the same DirectShow filter manages an entire category of hardware devices. In that case, the moniker represents the device, and the moniker is used to initialize the filter. The application can treat each device as a separate filter, regardless of the underlying implementation.

For more information on using this interface, see <a href="/windows/desktop/DirectShow/using-the-system-device-enumerator">Using the System Device Enumerator</a>.

## -inheritance

The <b>ICreateDevEnum</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreateDevEnum</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/interfaces">Interfaces</a>



<a href="/windows/desktop/DirectShow/using-the-system-device-enumerator">Using the System Device Enumerator</a>
