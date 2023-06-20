---
UID: NF:wmp.IWMPEvents3.CdromRipStateChange
title: IWMPEvents3::CdromRipStateChange (wmp.h)
description: The CdromRipStateChange event occurs when a CD ripping operation changes state.
helpviewer_keywords: ["CdromRipStateChange","CdromRipStateChange method [Windows Media Player]","CdromRipStateChange method [Windows Media Player]","IWMPEvents3 interface","IWMPEvents3 interface [Windows Media Player]","CdromRipStateChange method","IWMPEvents3.CdromRipStateChange","IWMPEvents3::CdromRipStateChange","IWMPEvents3CdromRipStateChange","wmp.iwmpevents3_iwmpevents3__cdromripstatechange","wmp/IWMPEvents3::CdromRipStateChange"]
old-location: wmp\iwmpevents3_iwmpevents3__cdromripstatechange.htm
tech.root: WMP
ms.assetid: 08445295-4fed-412f-84ce-eaf337758472
ms.date: 4/26/2023
ms.keywords: CdromRipStateChange, CdromRipStateChange method [Windows Media Player], CdromRipStateChange method [Windows Media Player],IWMPEvents3 interface, IWMPEvents3 interface [Windows Media Player],CdromRipStateChange method, IWMPEvents3.CdromRipStateChange, IWMPEvents3::CdromRipStateChange, IWMPEvents3CdromRipStateChange, wmp.iwmpevents3_iwmpevents3__cdromripstatechange, wmp/IWMPEvents3::CdromRipStateChange
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
 - IWMPEvents3::CdromRipStateChange
 - wmp/IWMPEvents3::CdromRipStateChange
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
 - IWMPEvents3.CdromRipStateChange
---

# IWMPEvents3::CdromRipStateChange


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>CdromRipStateChange</b> event occurs when a CD ripping operation changes state.

## -parameters

### -param pCdromRip [in]

Pointer to the <b>IWMPCdromRip</b> interface that represents the ripping operation that raised the error.

### -param wmprs [in]

<b>WMPRipState</b> enumeration value that indicates the new state.

## -remarks

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip">IWMPCdromRip Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpripstate">WMPRipState</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>