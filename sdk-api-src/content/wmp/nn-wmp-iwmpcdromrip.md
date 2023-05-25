---
UID: NN:wmp.IWMPCdromRip
title: IWMPCdromRip (wmp.h)
description: The IWMPCdromRip interface provides methods to manage copying, or ripping, tracks from an audio CD.Ripping a CD by using the IWMPCdromRip interface has the same effect as ripping music by using the Windows Media Player user interface.
helpviewer_keywords: ["IWMPCdromRip","IWMPCdromRip interface [Windows Media Player]","IWMPCdromRip interface [Windows Media Player]","described","IWMPCdromRipInterface","wmp.iwmpcdromrip","wmp/IWMPCdromRip"]
old-location: wmp\iwmpcdromrip.htm
tech.root: WMP
ms.assetid: c3e2db46-bef0-4c79-91b5-97ca5a86c6ba
ms.date: 4/26/2023
ms.keywords: IWMPCdromRip, IWMPCdromRip interface [Windows Media Player], IWMPCdromRip interface [Windows Media Player],described, IWMPCdromRipInterface, wmp.iwmpcdromrip, wmp/IWMPCdromRip
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
 - IWMPCdromRip
 - wmp/IWMPCdromRip
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
 - IWMPCdromRip
---

# IWMPCdromRip interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPCdromRip</b> interface provides methods to manage copying, or <i>ripping</i>, tracks from an audio CD.

Ripping a CD by using the <b>IWMPCdromRip</b> interface has the same effect as ripping music by using the Windows Media Player user interface. Ripped content is automatically added to the library according to the user's preferences. For more information about user preferences for CD ripping, see "Ripping music from CDs" in Windows Media Player Help.

## -inheritance

The <b>IWMPCdromRip</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPCdromRip</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="/windows/desktop/WMP/ripping-a-cd">Ripping a CD</a>
