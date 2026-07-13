---
UID: NN:wmp.IWMPEvents4
title: IWMPEvents4 (wmp.h)
description: The IWMPEvents4 interface provides access to an event originating from the Windows Media Player 12 control so that an application that has this control embedded in it can respond to the event.
helpviewer_keywords: ["IWMPEvents4","IWMPEvents4 interface [Windows Media Player]","IWMPEvents4 interface [Windows Media Player]","described","wmp.iwmpevents4","wmp/IWMPEvents4"]
old-location: wmp\iwmpevents4.htm
tech.root: WMP
ms.assetid: b846ef23-1206-4a0b-866f-558b99b73f1d
ms.date: 4/26/2023
ms.keywords: IWMPEvents4, IWMPEvents4 interface [Windows Media Player], IWMPEvents4 interface [Windows Media Player],described, wmp.iwmpevents4, wmp/IWMPEvents4
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents4
 - wmp/IWMPEvents4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPEvents4
---

# IWMPEvents4 interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents4</a> interface provides access to an event originating from the Windows Media Player 12 control so that an application that has this control embedded in it can respond to the event. The event exposed by <b>IWMPEvents4</b> is also exposed by the <a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents</a> interface.

## -inheritance

The <b>IWMPEvents4</b> interface inherits from <b>IWMPEvents3</b>. <b>IWMPEvents4</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/handling-events-in-c">Handling Events in C++</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>
