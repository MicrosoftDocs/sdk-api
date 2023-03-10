---
UID: NF:wmsecure.IWMGetSecureChannel.GetPeerSecureChannelInterface
title: IWMGetSecureChannel::GetPeerSecureChannelInterface (wmsecure.h)
description: The GetPeerSecureChannelInterface method gets the IWMSecureChannel interface from the other communication party.
helpviewer_keywords: ["GetPeerSecureChannelInterface","GetPeerSecureChannelInterface method [windows Media Format]","GetPeerSecureChannelInterface method [windows Media Format]","IWMGetSecureChannel interface","IWMGetSecureChannel interface [windows Media Format]","GetPeerSecureChannelInterface method","IWMGetSecureChannel.GetPeerSecureChannelInterface","IWMGetSecureChannel::GetPeerSecureChannelInterface","wmformat.iwmgetsecurechannel_getpeersecurechannelinterface","wmsecure/IWMGetSecureChannel::GetPeerSecureChannelInterface"]
old-location: wmformat\iwmgetsecurechannel_getpeersecurechannelinterface.htm
tech.root: wmformat
ms.assetid: bda30638-10b5-4288-b885-b63485606a7f
ms.date: 12/05/2018
ms.keywords: GetPeerSecureChannelInterface, GetPeerSecureChannelInterface method [windows Media Format], GetPeerSecureChannelInterface method [windows Media Format],IWMGetSecureChannel interface, IWMGetSecureChannel interface [windows Media Format],GetPeerSecureChannelInterface method, IWMGetSecureChannel.GetPeerSecureChannelInterface, IWMGetSecureChannel::GetPeerSecureChannelInterface, wmformat.iwmgetsecurechannel_getpeersecurechannelinterface, wmsecure/IWMGetSecureChannel::GetPeerSecureChannelInterface
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
 - IWMGetSecureChannel::GetPeerSecureChannelInterface
 - wmsecure/IWMGetSecureChannel::GetPeerSecureChannelInterface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsecure.h
api_name:
 - IWMGetSecureChannel.GetPeerSecureChannelInterface
---

# IWMGetSecureChannel::GetPeerSecureChannelInterface


## -description

<p class="CCE_Message">[<b>GetPeerSecureChannelInterface</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]

The <b>GetPeerSecureChannelInterface</b> method gets the <a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a> interface from the other communication party.

## -parameters

### -param ppPeer [out]

An address of a pointer to the other communication party's <a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmsecurechannel">IWMSecureChannel</a> object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/wmsecure/nn-wmsecure-iwmgetsecurechannel">IWMGetSecureChannel</a>