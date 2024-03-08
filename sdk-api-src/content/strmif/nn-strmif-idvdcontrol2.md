---
UID: NN:strmif.IDvdControl2
title: IDvdControl2 (strmif.h)
description: The IDvdControl2 interface navigates and plays DVD-Video titles.
helpviewer_keywords: ["IDvdControl2","IDvdControl2 interface [DirectShow]","IDvdControl2 interface [DirectShow]","described","IDvdControl2Interface","dshow.idvdcontrol2","strmif/IDvdControl2"]
old-location: dshow\idvdcontrol2.htm
tech.root: dshow
ms.assetid: eda43b20-1c4d-4769-bb87-3942716af13c
ms.date: 4/26/2023
ms.keywords: IDvdControl2, IDvdControl2 interface [DirectShow], IDvdControl2 interface [DirectShow],described, IDvdControl2Interface, dshow.idvdcontrol2, strmif/IDvdControl2
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - IDvdControl2
 - strmif/IDvdControl2
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
 - IDvdControl2
---

# IDvdControl2 interface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>IDvdControl2</code> interface navigates and plays DVD-Video titles. The DirectShow <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> source filter implements this interface. After creating a DVD filter graph through the <a href="/windows/desktop/api/strmif/nn-strmif-idvdgraphbuilder">IDvdGraphBuilder</a> interface, a DVD player application uses the methods of the <b>IDvdControl2</b> and <a href="/windows/desktop/api/strmif/nn-strmif-idvdinfo2">IDvdInfo2</a> interfaces to send DVD commands to and retrieve state information from the DVD Navigator.

<code>IDvdControl2</code> provides the full functionality required by the DVD Annex J specification, as well as methods for playback, menu navigation, and parental control. For more information on writing a DVD player application using the DVD Navigator, including topics on the DVD filter graph, command synchronization, parental controls, menus, and karaoke support, see <a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>.</p>Playback

## -inheritance

The <b>IDvdControl2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdControl2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>
