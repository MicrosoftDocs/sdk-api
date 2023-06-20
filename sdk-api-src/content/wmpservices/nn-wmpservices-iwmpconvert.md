---
UID: NN:wmpservices.IWMPConvert
title: IWMPConvert (wmpservices.h)
description: The IWMPConvert interface provides methods to enable Windows Media Player conversion plug-ins to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).
helpviewer_keywords: ["IWMPConvert","IWMPConvert interface [Windows Media Player]","IWMPConvert interface [Windows Media Player]","described","IWMPConvertInterface","wmp.iwmpconvert","wmpservices/IWMPConvert"]
old-location: wmp\iwmpconvert.htm
tech.root: WMP
ms.assetid: 316d1a13-0803-4414-8c51-0d5c4768b06d
ms.date: 4/26/2023
ms.keywords: IWMPConvert, IWMPConvert interface [Windows Media Player], IWMPConvert interface [Windows Media Player],described, IWMPConvertInterface, wmp.iwmpconvert, wmpservices/IWMPConvert
req.header: wmpservices.h
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
 - IWMPConvert
 - wmpservices/IWMPConvert
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPConvert
---

# IWMPConvert interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPConvert</b> interface provides methods to enable Windows Media Player conversion plug-ins to convert digital media files that are created using technologies not provided by Microsoft, into Advanced Systems Format (ASF).

## -inheritance

The <b>IWMPConvert</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPConvert</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

These methods are implemented by a conversion plug-in and called by Windows Media Player.

## -see-also

<a href="/windows/desktop/WMP/interfaces">Interfaces</a>
