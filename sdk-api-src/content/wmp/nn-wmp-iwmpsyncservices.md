---
UID: NN:wmp.IWMPSyncServices
title: IWMPSyncServices (wmp.h)
description: The IWMPSyncServices interface provides methods to enumerate available devices that can synchronize digital media files with Windows Media Player 10 or later.To use this interface, you must create a remoted instance of the Windows Media Player control.
helpviewer_keywords: ["IWMPSyncServices","IWMPSyncServices interface [Windows Media Player]","IWMPSyncServices interface [Windows Media Player]","described","IWMPSyncServicesInterface","wmp.iwmpsyncservices","wmp/IWMPSyncServices"]
old-location: wmp\iwmpsyncservices.htm
tech.root: WMP
ms.assetid: 57db3646-2f79-4087-98b2-2bc9d2f3c866
ms.date: 4/26/2023
ms.keywords: IWMPSyncServices, IWMPSyncServices interface [Windows Media Player], IWMPSyncServices interface [Windows Media Player],described, IWMPSyncServicesInterface, wmp.iwmpsyncservices, wmp/IWMPSyncServices
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
 - IWMPSyncServices
 - wmp/IWMPSyncServices
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
 - IWMPSyncServices
---

# IWMPSyncServices interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPSyncServices</b> interface provides methods to enumerate available devices that can synchronize digital media files with Windows Media Player 10 or later.

To use this interface, you must create a remoted instance of the Windows Media Player control.

## -inheritance

The <b>IWMPSyncServices</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPSyncServices</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
