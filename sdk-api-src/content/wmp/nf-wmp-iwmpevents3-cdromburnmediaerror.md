---
UID: NF:wmp.IWMPEvents3.CdromBurnMediaError
title: IWMPEvents3::CdromBurnMediaError (wmp.h)
description: The CdromBurnMediaError event occurs when an error happens while burning an individual media item to a CD.
helpviewer_keywords: ["CdromBurnMediaError","CdromBurnMediaError method [Windows Media Player]","CdromBurnMediaError method [Windows Media Player]","IWMPEvents3 interface","IWMPEvents3 interface [Windows Media Player]","CdromBurnMediaError method","IWMPEvents3.CdromBurnMediaError","IWMPEvents3::CdromBurnMediaError","IWMPEvents3CdromBurnMediaError","wmp.iwmpevents3_iwmpevents3__cdromburnmediaerror","wmp/IWMPEvents3::CdromBurnMediaError"]
old-location: wmp\iwmpevents3_iwmpevents3__cdromburnmediaerror.htm
tech.root: WMP
ms.assetid: 4bad9de2-8899-4149-965c-7835bd854f6f
ms.date: 4/26/2023
ms.keywords: CdromBurnMediaError, CdromBurnMediaError method [Windows Media Player], CdromBurnMediaError method [Windows Media Player],IWMPEvents3 interface, IWMPEvents3 interface [Windows Media Player],CdromBurnMediaError method, IWMPEvents3.CdromBurnMediaError, IWMPEvents3::CdromBurnMediaError, IWMPEvents3CdromBurnMediaError, wmp.iwmpevents3_iwmpevents3__cdromburnmediaerror, wmp/IWMPEvents3::CdromBurnMediaError
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
 - IWMPEvents3::CdromBurnMediaError
 - wmp/IWMPEvents3::CdromBurnMediaError
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
 - IWMPEvents3.CdromBurnMediaError
---

# IWMPEvents3::CdromBurnMediaError


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CdromBurnMediaError</b> event occurs when an error happens while burning an individual media item to a CD.

## -parameters

### -param pCdromBurn [in]

Pointer to the <b>IWMPCdromBurn</b> interface that represents the burning operation that raised the error.

### -param pMedia [in]

Pointer to the <b>IDispatch</b> interface that represents the media item that raised the error. Call <b>QueryInterface</b> through this pointer to retrieve a pointer to <b>IWMPMedia</b>.

## -remarks

To capture generic errors, handle the <b>CdromBurnError</b> event.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror">IWMPEvents3::CdromBurnError</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>