---
UID: NN:wmp.IWMPPlayer3
title: IWMPPlayer3 (wmp.h)
description: The IWMPPlayer3 interface provides methods for modifying the basic behavior of the control user interface. These methods supplement the IWMPCore2 interface.
helpviewer_keywords: ["IWMPPlayer3","IWMPPlayer3 interface [Windows Media Player]","IWMPPlayer3 interface [Windows Media Player]","described","IWMPPlayer3Interface","wmp.iwmpplayer3","wmp/IWMPPlayer3"]
old-location: wmp\iwmpplayer3.htm
tech.root: WMP
ms.assetid: 0d8a9414-5c5c-40e0-a34c-430ead01ef26
ms.date: 4/26/2023
ms.keywords: IWMPPlayer3, IWMPPlayer3 interface [Windows Media Player], IWMPPlayer3 interface [Windows Media Player],described, IWMPPlayer3Interface, wmp.iwmpplayer3, wmp/IWMPPlayer3
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
 - IWMPPlayer3
 - wmp/IWMPPlayer3
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
 - IWMPPlayer3
---

# IWMPPlayer3 interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPPlayer3</b> interface provides methods for modifying the basic behavior of the control user interface. These methods supplement the <b>IWMPCore2</b> interface.



The <b>IWMPPlayer3</b> interface duplicates the methods of <b>IWMPPlayer</b> and <b>IWMPPlayer2</b> and inherits the methods of <b>IWMPCore2</b>. It is identical to <b>IWMPPlayer2</b> except for the inherited interface.

Retrieve a pointer to an <b>IWMPPlayer3</b> interface either by calling the <b>QueryInterface</b> method of the <b>IWMPPlayer</b> or <b>IWMPPlayer2</b> interface, or by calling the COM <b>CoCreateInstance</b> method.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore">IWMPCore Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore2">IWMPCore2 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcore3">IWMPCore3 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer2">IWMPPlayer2 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpplayer4">IWMPPlayer4 Interface</a>



<a href="/windows/desktop/WMP/interfaces">Interfaces</a>