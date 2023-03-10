---
UID: NN:strmif.IDvdState
title: IDvdState (strmif.h)
description: The IDvdState interface caches the current state.The object that implements this interface is called a DVD bookmark. You can use it to save and restore the DVD state, which includes the playback location, the user's parental level, and the DVD region.
helpviewer_keywords: ["IDvdState","IDvdState interface [DirectShow]","IDvdState interface [DirectShow]","described","IDvdStateInterface","dshow.idvdstate","strmif/IDvdState"]
old-location: dshow\idvdstate.htm
tech.root: dshow
ms.assetid: df30a3b9-7541-42a8-b642-3b6450a0345e
ms.date: 12/05/2018
ms.keywords: IDvdState, IDvdState interface [DirectShow], IDvdState interface [DirectShow],described, IDvdStateInterface, dshow.idvdstate, strmif/IDvdState
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
 - IDvdState
 - strmif/IDvdState
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
 - IDvdState
---

# IDvdState interface


## -description

The <b>IDvdState</b> interface caches the current state.

The object that implements this interface is called a <i>DVD bookmark</i>. You can use it to save and restore the DVD state, which includes the playback location, the user's parental level, and the DVD region.

## -inheritance

The <b>IDvdState</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdState</b> also has these types of members:

## -remarks

To get the current DVD state information from the <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a>, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getstate">IDvdInfo2::GetState</a>. To restore the state, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setstate">IDvdControl2::SetState</a>.

The DVD bookmark object also implements <b>IPersistStream</b> and <b>IPersistMemory</b>. You can use these interfaces to persist the state. You can also create an empty bookmark object by calling <b>CoCreateInstance</b>. The object's CLSID is CLSID_DVDState, defined in uuids.h.

Prior to Windows Vista, a bookmark can be used only on the same computer where it was created. Starting in Windows Vista, the DVD Navigator is able to create bookmarks that can be used other computers. To enable this feature, call <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setoption">IDvdControl2::SetOption</a> with the DVD_EnablePortableBookmarks flag, before calling <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getstate">GetState</a> or <a href="/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-setstate">SetState</a>.

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>
