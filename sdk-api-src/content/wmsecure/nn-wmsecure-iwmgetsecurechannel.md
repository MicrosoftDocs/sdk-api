---
UID: NN:wmsecure.IWMGetSecureChannel
title: IWMGetSecureChannel (wmsecure.h)
description: The IWMGetSecureChannel interface is used by one communication party to get the other party's IWMSecureChannel interface.
helpviewer_keywords: ["IWMGetSecureChannel","IWMGetSecureChannel interface [windows Media Format]","IWMGetSecureChannel interface [windows Media Format]","described","wmformat.iwmgetsecurechannel","wmsecure/IWMGetSecureChannel"]
old-location: wmformat\iwmgetsecurechannel.htm
tech.root: wmformat
ms.assetid: 0ebb380a-5c14-4630-8ae4-825809f4737a
ms.date: 12/05/2018
ms.keywords: IWMGetSecureChannel, IWMGetSecureChannel interface [windows Media Format], IWMGetSecureChannel interface [windows Media Format],described, wmformat.iwmgetsecurechannel, wmsecure/IWMGetSecureChannel
req.header: wmsecure.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IWMGetSecureChannel
 - wmsecure/IWMGetSecureChannel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsecure.h
api_name:
 - IWMGetSecureChannel
---

# IWMGetSecureChannel interface


## -description

<p class="CCE_Message">[<b>IWMGetSecureChannel</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

The <b>IWMGetSecureChannel</b> interface is used by one communication party to get the
 other party's <a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a> interface.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMGetSecureChannel</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMGetSecureChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMGetSecureChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/wmsecure/nf-wmsecure-iwmgetsecurechannel-getpeersecurechannelinterface">GetPeerSecureChannelInterface</a>
</td>
<td align="left" width="63%">
Gets the <a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a> interface from the other communication party.

</td>
</tr>
</table>