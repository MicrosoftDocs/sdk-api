---
UID: NN:contentpartner.IWMPContentPartner
title: IWMPContentPartner (contentpartner.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPContentPartner","IWMPContentPartner interface [Windows Media Player]","IWMPContentPartner interface [Windows Media Player]","described","IWMPContentPartnerInterface","contentpartner/IWMPContentPartner","wmp.iwmpcontentpartner"]
old-location: wmp\iwmpcontentpartner.htm
tech.root: WMP
ms.assetid: 2078ebd4-3570-4c39-9081-1b55d9e8286f
ms.date: 12/05/2018
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

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>IWMPContentPartner</b> interface provides methods that Windows Media Player calls to integrate its user interface with an online store's catalog and services. This interface is implemented by a content partner plug-in, which is provided by the online store.

## -inheritance

The <b>IWMPContentPartner</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPContentPartner</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/reference-for-type-1-online-stores">Reference for Type 1 Online Stores</a>
