---
UID: NF:wmsecure.IWMGetSecureChannel.GetPeerSecureChannelInterface
title: IWMGetSecureChannel::GetPeerSecureChannelInterface (wmsecure.h)
description: The GetPeerSecureChannelInterface method gets the IWMSecureChannel interface from the other communication party.
helpviewer_keywords: ["GetPeerSecureChannelInterface","GetPeerSecureChannelInterface method [windows Media Format]","GetPeerSecureChannelInterface method [windows Media Format]","IWMGetSecureChannel interface","IWMGetSecureChannel interface [windows Media Format]","GetPeerSecureChannelInterface method","IWMGetSecureChannel.GetPeerSecureChannelInterface","IWMGetSecureChannel::GetPeerSecureChannelInterface","wmformat.iwmgetsecurechannel_getpeersecurechannelinterface","wmsecure/IWMGetSecureChannel::GetPeerSecureChannelInterface"]
old-location: wmformat\iwmgetsecurechannel_getpeersecurechannelinterface.htm
tech.root: wmformat
ms.assetid: bda30638-10b5-4288-b885-b63485606a7f
ms.date: 4/26/2023
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

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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