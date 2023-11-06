---
UID: NF:wmp.IWMPEvents.MediaError
title: IWMPEvents::MediaError (wmp.h)
description: The MediaError event occurs when the Media object has an error condition.
helpviewer_keywords: ["IWMPEvents interface [Windows Media Player]","MediaError method","IWMPEvents.MediaError","IWMPEvents::MediaError","IWMPEventsMediaError","MediaError","MediaError method [Windows Media Player]","MediaError method [Windows Media Player]","IWMPEvents interface","wmp.iwmpevents_iwmpevents__mediaerror","wmp/IWMPEvents::MediaError"]
old-location: wmp\iwmpevents_iwmpevents__mediaerror.htm
tech.root: WMP
ms.assetid: 3c48ff94-01d6-492c-912c-ee74b619730b
ms.date: 4/26/2023
ms.keywords: IWMPEvents interface [Windows Media Player],MediaError method, IWMPEvents.MediaError, IWMPEvents::MediaError, IWMPEventsMediaError, MediaError, MediaError method [Windows Media Player], MediaError method [Windows Media Player],IWMPEvents interface, wmp.iwmpevents_iwmpevents__mediaerror, wmp/IWMPEvents::MediaError
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
 - IWMPEvents::MediaError
 - wmp/IWMPEvents::MediaError
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
 - IWMPEvents.MediaError
---

# IWMPEvents::MediaError


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MediaError</b> event occurs when the <b>Media</b> object has an error condition.

## -parameters

### -param pMediaObject [in]

Pointer to an <b>IDispatch</b> interface for the object that has an error condition.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>