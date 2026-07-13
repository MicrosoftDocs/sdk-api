---
UID: NF:wmp.IWMPEvents3.LibraryDisconnect
title: IWMPEvents3::LibraryDisconnect (wmp.h)
description: The LibraryDisconnect event occurs when a library is no longer available.
helpviewer_keywords: ["IWMPEvents3 interface [Windows Media Player]","LibraryDisconnect method","IWMPEvents3.LibraryDisconnect","IWMPEvents3::LibraryDisconnect","IWMPEvents3LibraryDisconnect","LibraryDisconnect","LibraryDisconnect method [Windows Media Player]","LibraryDisconnect method [Windows Media Player]","IWMPEvents3 interface","wmp.iwmpevents3_iwmpevents3__librarydisconnect","wmp/IWMPEvents3::LibraryDisconnect"]
old-location: wmp\iwmpevents3_iwmpevents3__librarydisconnect.htm
tech.root: WMP
ms.assetid: eb0f4d9f-23b7-4fe7-b45d-152a2f64af30
ms.date: 4/26/2023
ms.keywords: IWMPEvents3 interface [Windows Media Player],LibraryDisconnect method, IWMPEvents3.LibraryDisconnect, IWMPEvents3::LibraryDisconnect, IWMPEvents3LibraryDisconnect, LibraryDisconnect, LibraryDisconnect method [Windows Media Player], LibraryDisconnect method [Windows Media Player],IWMPEvents3 interface, wmp.iwmpevents3_iwmpevents3__librarydisconnect, wmp/IWMPEvents3::LibraryDisconnect
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
 - IWMPEvents3::LibraryDisconnect
 - wmp/IWMPEvents3::LibraryDisconnect
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
 - IWMPEvents3.LibraryDisconnect
---

# IWMPEvents3::LibraryDisconnect


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>LibraryDisconnect</b> event occurs when a library is no longer available.

## -parameters

### -param pLibrary [in]

Pointer to the <b>IWMPLibrary</b> interface that represents the library that disconnected.

## -remarks

This event does not occur for the local library.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibrary">IWMPLibrary Interface</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>