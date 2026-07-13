---
UID: NN:contentpartner.IWMPContentPartner
title: IWMPContentPartner (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartner","IWMPContentPartner interface [Windows Media Player]","IWMPContentPartner interface [Windows Media Player]","described","IWMPContentPartnerInterface","contentpartner/IWMPContentPartner","wmp.iwmpcontentpartner"]
old-location: wmp\iwmpcontentpartner.htm
tech.root: WMP
ms.assetid: 2078ebd4-3570-4c39-9081-1b55d9e8286f
ms.date: 4/26/2023
ms.keywords: IWMPContentPartner, IWMPContentPartner interface [Windows Media Player], IWMPContentPartner interface [Windows Media Player],described, IWMPContentPartnerInterface, contentpartner/IWMPContentPartner, wmp.iwmpcontentpartner
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
 - IWMPContentPartner
 - contentpartner/IWMPContentPartner
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
 - IWMPContentPartner
---

# IWMPContentPartner interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentPartner</b> interface provides methods that Windows Media Player calls to integrate its user interface with an online store's catalog and services. This interface is implemented by a content partner plug-in, which is provided by the online store.

## -inheritance

The <b>IWMPContentPartner</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPContentPartner</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/reference-for-type-1-online-stores">Reference for Type 1 Online Stores</a>
