---
UID: NN:wmsecure.IWMGetSecureChannel
title: IWMGetSecureChannel (wmsecure.h)
description: The IWMGetSecureChannel interface is used by one communication party to get the other party's IWMSecureChannel interface.
old-location: wmformat\iwmgetsecurechannel.htm
tech.root: wmformat
ms.assetid: 0ebb380a-5c14-4630-8ae4-825809f4737a
ms.date: 12/05/2018
ms.keywords: IWMGetSecureChannel, IWMGetSecureChannel interface [windows Media Format], IWMGetSecureChannel interface [windows Media Format],described, wmformat.iwmgetsecurechannel, wmsecure/IWMGetSecureChannel
f1_keywords:
- wmsecure/IWMGetSecureChannel
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- wmsecure.h
api_name:
- IWMGetSecureChannel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMGetSecureChannel interface


## -description


<p class="CCE_Message">[<b>IWMGetSecureChannel</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

The <b>IWMGetSecureChannel</b> interface is used by one communication party to get the
 other party's <a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMGetSecureChannel</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMGetSecureChannel</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nf-wmsecure-iwmgetsecurechannel-getpeersecurechannelinterface">GetPeerSecureChannelInterface</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a> interface from the other communication party.

</td>
</tr>
</table> 

