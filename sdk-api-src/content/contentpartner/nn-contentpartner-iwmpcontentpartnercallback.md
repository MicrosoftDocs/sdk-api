---
UID: NN:contentpartner.IWMPContentPartnerCallback
title: IWMPContentPartnerCallback (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartnerCallback","IWMPContentPartnerCallback interface [Windows Media Player]","IWMPContentPartnerCallback interface [Windows Media Player]","described","IWMPContentPartnerCallbackInterface","contentpartner/IWMPContentPartnerCallback","wmp.iwmpcontentpartnercallback"]
old-location: wmp\iwmpcontentpartnercallback.htm
tech.root: WMP
ms.assetid: 3c66052b-2b82-44aa-868d-5d5a4501c457
ms.date: 4/26/2023
ms.keywords: IWMPContentPartnerCallback, IWMPContentPartnerCallback interface [Windows Media Player], IWMPContentPartnerCallback interface [Windows Media Player],described, IWMPContentPartnerCallbackInterface, contentpartner/IWMPContentPartnerCallback, wmp.iwmpcontentpartnercallback
req.header: contentpartner.h
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
 - IWMPContentPartnerCallback
 - contentpartner/IWMPContentPartnerCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - contentpartner.h
api_name:
 - IWMPContentPartnerCallback
---

# IWMPContentPartnerCallback interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentPartnerCallback</b> interface provides methods, implemented by Windows Media Player, that a content partner plug-in calls to integrate its catalog and services with the Windows Media Player user interface.

## -inheritance

The <b>IWMPContentPartnerCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPContentPartnerCallback</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/reference-for-type-1-online-stores">Reference for Type 1 Online Stores</a>
