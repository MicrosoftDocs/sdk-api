---
UID: NF:wmp.IWMPEvents3.LibraryConnect
title: IWMPEvents3::LibraryConnect (wmp.h)
description: The LibraryConnect event occurs when a library becomes available.
helpviewer_keywords: ["IWMPEvents3 interface [Windows Media Player]","LibraryConnect method","IWMPEvents3.LibraryConnect","IWMPEvents3::LibraryConnect","IWMPEvents3LibraryConnect","LibraryConnect","LibraryConnect method [Windows Media Player]","LibraryConnect method [Windows Media Player]","IWMPEvents3 interface","wmp.iwmpevents3_iwmpevents3__libraryconnect","wmp/IWMPEvents3::LibraryConnect"]
old-location: wmp\iwmpevents3_iwmpevents3__libraryconnect.htm
tech.root: WMP
ms.assetid: b9e1feb7-c894-4f37-9756-378740637f6e
ms.date: 4/26/2023
ms.keywords: IWMPEvents3 interface [Windows Media Player],LibraryConnect method, IWMPEvents3.LibraryConnect, IWMPEvents3::LibraryConnect, IWMPEvents3LibraryConnect, LibraryConnect, LibraryConnect method [Windows Media Player], LibraryConnect method [Windows Media Player],IWMPEvents3 interface, wmp.iwmpevents3_iwmpevents3__libraryconnect, wmp/IWMPEvents3::LibraryConnect
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
 - IWMPEvents3::LibraryConnect
 - wmp/IWMPEvents3::LibraryConnect
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
 - IWMPEvents3.LibraryConnect
---

# IWMPEvents3::LibraryConnect


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>LibraryConnect</b> event occurs when a library becomes available.

## -parameters

### -param pLibrary [in]

Pointer to the <b>IWMPLibrary</b> interface that represents the library that connected.

## -remarks

This event does not occur for the local library.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmplibrary">IWMPLibrary Interface</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>