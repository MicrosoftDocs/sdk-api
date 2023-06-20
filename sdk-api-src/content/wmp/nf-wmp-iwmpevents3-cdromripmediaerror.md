---
UID: NF:wmp.IWMPEvents3.CdromRipMediaError
title: IWMPEvents3::CdromRipMediaError (wmp.h)
description: The CdromRipMediaError event occurs when an error happens while ripping an individual track from a CD.
helpviewer_keywords: ["CdromRipMediaError","CdromRipMediaError method [Windows Media Player]","CdromRipMediaError method [Windows Media Player]","IWMPEvents3 interface","IWMPEvents3 interface [Windows Media Player]","CdromRipMediaError method","IWMPEvents3.CdromRipMediaError","IWMPEvents3::CdromRipMediaError","IWMPEvents3CdromRipMediaError","wmp.iwmpevents3_iwmpevents3__cdromripmediaerror","wmp/IWMPEvents3::CdromRipMediaError"]
old-location: wmp\iwmpevents3_iwmpevents3__cdromripmediaerror.htm
tech.root: WMP
ms.assetid: 103f6d52-5b59-422d-918d-5004cbdfc75a
ms.date: 4/26/2023
ms.keywords: CdromRipMediaError, CdromRipMediaError method [Windows Media Player], CdromRipMediaError method [Windows Media Player],IWMPEvents3 interface, IWMPEvents3 interface [Windows Media Player],CdromRipMediaError method, IWMPEvents3.CdromRipMediaError, IWMPEvents3::CdromRipMediaError, IWMPEvents3CdromRipMediaError, wmp.iwmpevents3_iwmpevents3__cdromripmediaerror, wmp/IWMPEvents3::CdromRipMediaError
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
req.target-min-winversvr: 
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents3::CdromRipMediaError
 - wmp/IWMPEvents3::CdromRipMediaError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents3.CdromRipMediaError
---

# IWMPEvents3::CdromRipMediaError


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CdromRipMediaError</b> event occurs when an error happens while ripping an individual track from a CD.

## -parameters

### -param pCdromRip [in]

Pointer to the <b>IWMPCdromRip</b> interface that represents the ripping operation that raised the error.

### -param pMedia [in]

Pointer to the <b>IDispatch</b> interface that represents the media item that raised the error. Call <b>QueryInterface</b> through this pointer to retrieve a pointer to <b>IWMPMedia</b>.

## -remarks

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip">IWMPCdromRip Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>